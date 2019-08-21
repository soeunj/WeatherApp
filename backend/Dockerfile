FROM node:10-alpine

WORKDIR /weatherapp/backend

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 9000

CMD ["npm", "run", "dev"]
