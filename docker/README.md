# Docker Notes

## Theory

### Image

An image is a filesystem and parameters to use at runtime. It doesn’t have state and never changes. 

### Container

A container is a running instance of an image. 


## Useful Docker commands

Find the ip of the docker machine

`docker-machine ip`

Find environment variables for docker machine

`docker-machine env`

List docker containers

`docker ps`

List all docker containers including stopped

`docker ps -a`

List all docker images

`docker images` 

Remove all docker containers

`docker rm $(docker ps -aq)`

Remove all docker images

`docker rmi $(docker images -aq)`      

Test docker installation

`docker run hello-world` 


## Useful quick containers

Run Ubuntu bash terminal

```

docker run -it ubuntu   /bin/bash
                 |          |
                Name of   Name of  
                ubuntu    command 
                official  to run
                image     after container
                          is loaded

-i interactive container with STDIN
-t teletype terminal

```

Start a stopped container with terminal

`docker start -i <container_name>`





