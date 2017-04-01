# Docker Stack(docker-compose.v3) and Docker Swarm

Create a new docker machine using virtualbox

`docker-machine create --driver virtualbox <machine-name>` 

Get IP of a machine by name

`docker-machine ip <machine-name>`

Get environment for machine by name

`docker-machine env <machine-name>`  

SSH to a docker machine

`docker-machine ssh <machine-name>` 

Select a docker-machine from the available machines

`eval $(docker-machine env <machine-name>`


## Initialize a Swarm

SSH to a docker machine

`docker-machine ssh <machine-name>`

Initialize swarm on the machine

`docker swarm init --advertise-addr <Machine-IP from docker-machine ls or docker-machine ip <machine-name>`  

Follow instructions to join any other machine to the swarm

List nodes in the swarm

`docker node ls` 
