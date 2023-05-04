
# EMQX docker setup

##  Description

The `public` directory contains the emqx image from the docker public registory.
And the `private` directory contains the emqx image from our private registry.

## Commands
You can use the docker compose command to start the docker service.
Follow the below steps to start the docker service
1. Go to your preferred directory `public` or `private`
2. Run `docker` command based on you docker compose version

_For docker compose version ( <2.0.0 )_
> docker-compose up

_For docker compose version ( >2.0.0 )_
> docker compose up

### Alternate way ( docker cli )
Run the following commands directly in your command-line interface.
_For `public` image_
> docker run -d --restart on-failure --name emqx -p 1883:1883 -p 8083:8083 -p 8084:8084 -p 8883:8883 -p 18083:18083 emqx/emqx:v4.0.13

_For `private` image_
> docker run -d --restart on-failure --name emqx -p 1883:1883 -p 8083:8083 -p 8084:8084 -p 8883:8883 -p 18083:18083 registry.patr.cloud/8d8518bc8af540419b20998b75201720/emqx
