# dockerized-react
dockerized-react
## Using Volumes in docker-compose(development stage)
Volume feature will map the specified folders in the container up against the folders in the working directory on the host machine(computer)
so that the new changes outside of the container will be reflected in the container(The volumes will hold the reference in the container to 
the files on the host machine.) The feature is really useful in the development because the changes will be reflected immediately in the running
container.

`docker-compose up`

## Using multi-stage docker file
Docker container can load more than one base image and allows us to set up different stages.
For example, we might wanna load the base image of node.js for building the html, js, css files from our react project and 
then serve these files up by the nginx server.

`docker build .`

`docker run -p 3000(the port on the host machine):80(nginx default port) <image id>`
