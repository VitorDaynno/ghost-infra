FROM node:dubnium-alpine

EXPOSE 5001

RUN apk add git

RUN git clone https://github.com/VitorDaynno/ghost.git /app && \
    cd /app && \
    yarn install --prod

WORKDIR /app 

CMD [ "yarn", "start" ]
