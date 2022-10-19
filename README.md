# Consumer rabitqueues and publish to rocket chat
[![CI](https://github.com/brunojhovany/rabbitmq-rocketchat-publisher/actions/workflows/main.yaml/badge.svg)](https://github.com/brunojhovany/rabbitmq-rocketchat-publisher/actions/workflows/main.yaml)[![Docker](https://img.shields.io/docker/cloud/build/eaudeweb/scratch?label=Docker&style=flat)](https://hub.docker.com/r/jhovanylinkin/rabbitmq-rocketchat-publisher/general)

This project is to publish messages from the rabbit queue to a rocket chat channel, you must first create a user and password that the app will use. This project arose from the need to have an error monitor in a data migration process, this simply notified that the program could not resolve said migration and there had to be human intervention.

Firts you need create `.env` file and put yours credentials access
```bash
RABBIT_HOST=
RABBIT_PORT=
RABBIT_USERNAME=
RABBIT_PASSWORD=
RABBIT_QUEUE=
RABBIT_EXCHANGE=
RABBIT_ROUTING_KEY=


ROCKET_SERVER=
ROCKET_PORT=
ROCKET_USER=
ROCKET_EMAIL=
ROCKET_PASSWORD=
```

## Run
for development you can use docker-compose.debug.yaml
```bash
docker-compose up -d -f docker-compose.debug.yaml
```
### run with docker-compose
you can run on windows or linux but if you prefer you can use a docker image for that.
`docker pull jhovanylinkin/rabbitmq-rocketchat-publisher:tagname`

example with docker-compose
```bash
docker-compose up -d
```
