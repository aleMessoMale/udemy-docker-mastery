FROM node:6-alpine

EXPOSE 3000

RUN apk add --update tini

WORKDIR /usr/src/app

COPY . .

RUN npm install && npm cache clean --force

COPY . .

CMD [ "/sbin/tini", "--", "node", "./bin/www" ]
