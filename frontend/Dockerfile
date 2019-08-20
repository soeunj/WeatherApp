FROM node:10-alpine

WORKDIR /weatherapp/frontend

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 8000

CMD npm start

