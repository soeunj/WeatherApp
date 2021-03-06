# WeatherApp

There was a beautiful idea of building an app that would show the upcoming weather. The developers wrote a nice backend and a frontend following the latest principles and - to be honest - bells and whistles. However, the developers did not remember to add any information about the infrastructure or even setup instructions in the source code.

Luckily we now have docker compose saving us from installing the tools on our computer, and making sure the app looks (and is) the same in development and in production. All we need is someone to add the few missing files!

## Prerequisites
- An [openweathermap](http://openweathermap.org) API key.
- [Docker](https://www.docker.com) and docker compose installed.
- Create .env file for API key under your project directory (If you want to store .env file in other directory, please edit docker-compose.yml file):
```
APPID=<<YOUR API KEY>>
```

## Instruction

To start up weatherapp:
```
docker-compose up
```
To build a docker image e.g. backend:
```
docker build -t weatherapp_backend .
```
To run the docker image e.g. backend:
```
docker run --env-file <<YOUR .env FILE PATH>> --rm -i -p 9000:9000 --name weatherapp_backend -t weatherapp_backend
```
If you want to run the app locally, run the following command under backend and frontend directory:
```
npm i && npm start
```

### DONE:
- Get an API key to make queries in the openweathermap
- Add Dockerfile's in the frontend and the backend directories
- Add a docker-compose.yml -file connecting the frontend and the backend, enabling running the app in a connected set of containers
- Add API for fetching forecast
- Share the development files for the container by using volumes, and make sure the containers are started with a command enabling hot reload.
- Fix eslint errors.

### TODO:
- Display forecast in frontend
- Check the browser location to refer for making a forecast
- Set up the weather service in a free cloud hosting service, e.g. AWS or Google Cloud
- Write ansible playbooks for installing docker and the app itself
