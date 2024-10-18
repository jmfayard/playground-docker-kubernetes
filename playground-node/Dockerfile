FROM node:latest

LABEL version="0.01"

WORKDIR /app

COPY . /app/

RUN npm install

EXPOSE 4000

CMD [ "node", "server.js" ]

