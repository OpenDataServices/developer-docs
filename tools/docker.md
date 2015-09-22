Docker
======



## Build an image

Docker builds and image from a file called `Dockerfile`

    docker build -t <somename> <path to Dockerfile>

For example (where a file called 'Dockerfile' is in the current working directory)

    docker build -t lodspeaker .

## Run an image to create a contianer

You then run an image to create a container

    docker run --publish=127.0.0.2:80:80 lodspeakr

## Inspect a container
You can inspect that container..

### List processes

    sudo docker ps

and you can 

#### Inspect processes

    sudo docker inspect <some identifier, e.g. Name, ID, etc>
