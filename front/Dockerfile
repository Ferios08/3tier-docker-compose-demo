FROM node:lts   

RUN apk update && apk upgrade && \
    apk add --no-cache bash git
WORKDIR /home/node/app
RUN git clone https://github.com/Ferios08/Angular-RestAPI-Demo.git /home/node/app


USER node


COPY --chown=node:node . .

CMD [ "ls" ]