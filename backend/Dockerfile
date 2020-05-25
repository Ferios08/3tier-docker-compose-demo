FROM node:lts   
RUN apt-get update && apt-get install -y git
WORKDIR /home/node/app
RUN git clone https://github.com/Ferios08/Angular-RestAPI-Demo.git /home/node/app

RUN npm install

ENV PORT=
ENV MONGO_URL=
ENV MONGO_USER=
ENV MONGO_PASS=
ENV MONGO_DB=
EXPOSE $PORT
CMD [ "node", "index.js" ]