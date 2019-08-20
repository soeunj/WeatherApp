FROM node:10

WORKDIR /weatherapp/backend

RUN npm install nodemon -g

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 9000

CMD npm start
