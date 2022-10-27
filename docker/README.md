# Docker

## What is Docker?

Docker is an open source platform that enables the building and management of containers. It is a platform as a service platform, as it provides an OS-level virtualisation. 

It is linked to a global repository known as Docker Hub. Docker images can be stored in repositories on Docker Hub. A Docker image is a file used to build a specifically configured container. 

## What is a Dockerfile?

It is a text document that contains all the commands, that a user can typically input into the command line, to build an image. To build the image detailed in a Dockerfile, the path of the Dockerfile has to be specified. 

## What is docker-compose.yml?

This is a tool that helps define and share multi-container applications. It creates a network and specifies dependencies for application that use a distributed architecture. 

## Basic Docker Commands

- `docker images`- lists all the images with details
- `docker ps`- lists all the containers and can be accompanied by other options
- `docker build -t <tag> <Dockerfile-location>`- this builds an image from the Dockerfile in that file location and then gives it a tag
- `docker run <image id>`- creates a running container of the specified image ID
- `docker exec -it <container id> bash`- allows you to interact with the container OS via a Bash terminal 
- `docker stop <container id>`- stops the specified container
- `docker start <container id>`- starts the specified container
- `docker rm <container id>`- removes the container
- `docker rmi <container id>`- removes the images
- `docker login`- login to Docker registry
- `docker push <username/image-name>:<tag>`- pushes the docker image to your Docker repository 
- `docker cp <src> <dest>`- copy files between a container and the local filesystem

## nginx_test

For this task, the base image was a prebuilt nginx image from the global Docker repository. The only required step was to replace the default html file with the custom html file `index.html`.

The command `docker run --expose 80:80 <image id>` was used to then run the image, so the custom html site can be viewed on port 80 on the localhost.

## node_app

This task was to deploy a two-tier architecture, with each tier (the application logic and the database) in a separate tier. 

For the database, the base image was a prebuilt mongo image from the global Docker repository. The only required changes to the image was to expose all IP ranges by replacing the `mongod.conf` file and exposing port 27017 for the database to run.

For the NodeJS application, the base image was node. The Docker file had a few more provisioning and configuration changes that can be viewed in the relevant `Dockerfile` in the `app` folder. The main commands in the script are the configuration of the application commands and the exposing of port 3000. All the file dependencies were copied from the localhost to the container. 

To run this two-tier architecture application, a `docker-compose.yml` file was utilised to connect the application layer and the database layer and to start them in a specified order. The following command was used to build the services- `sudo docker-compose build`. Then to run the services- `sudo docker-compose up`. 

## personal_webpage

These step are similar to those details in the `nginx` task. 

## How to push to Docker Hub

- `docker login`
- `docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]`
- `docker push TARGET_IMAGE[:TAG]`