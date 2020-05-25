FROM node:lts   
RUN apt-get update && apt-get install -y git
WORKDIR /app
RUN git clone https://github.com/Ferios08/NodeJS-Demo.git /app

RUN npm install
RUN chmod +x /app/scripts/wait-for.sh

ENV PORT=3000
ENV MONGO_URL="database"
ENV MONGO_USER="ferios"
ENV MONGO_PASS="admin"
ENV MONGO_DB="users"
EXPOSE $PORT
CMD [ "node", "index.js" ]