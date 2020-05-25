FROM node:lts as node
RUN apt-get update && apt-get install -y git
WORKDIR /app
RUN git clone https://github.com/Ferios08/NodeJS-Demo.git /app
RUN rm Dockerfile
RUN npm install
RUN npm run build
################################
# stage 2
FROM nginx
# client is the app name
COPY --from=node /app/dist/client /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]