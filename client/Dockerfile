FROM node:16.20.1-alpine3.17

WORKDIR /client

COPY package*.json .

RUN npm install

COPY . .

RUN ["npm", "start"]

EXPOSE 3000
