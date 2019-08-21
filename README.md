# WeatherApp

DONE:
- Get an API key to make queries in the openweathermap
- Add Dockerfile's in the frontend and the backend directories
- Add a docker-compose.yml -file connecting the frontend and the backend, enabling running the app in a connected set of containers
- Add API for fetching forecast
- Share the development files for the container by using volumes, and make sure the containers are started with a command enabling hot reload.
- Fix eslint errors.

TODO:
- Display forecast in frontend
- Check the browser location to refer for making a forecast

## Prerequisites
- An [openweathermap](http://openweathermap.org) API key.
- [Docker](https://www.docker.com) and docker compose installed.

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
docker run --rm -i -p 9000:9000 --name weatherapp_backend -t weatherapp_backend
```
If you want to run the app locally, run the following command under backend and frontend directory:
```
npm i && npm start
```
