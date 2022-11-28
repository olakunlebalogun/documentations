# Docker

## Documentation  


To get the documentation for a particular command  
`docker <verb> --help`

To get the overall commands  
`docker --help`


## Containers and Images Status

To check the running containers  
`docker ps`

To check all containers  
`docker ps -a`

To get all containers IDs  
`docker ps -aq`

To get containers and their sizes  
`docker ps -as`

To check all images  
`docker images` OR `docker image ls` 

## Running Containers  

To run a container from an Image *id* - *12345* on port *4000*  
`docker run -p 4000:2000 12345`

To run a containers on multiple ports from a single image in detached mode  
`docker run -p 4000:2000 -p 3000:2000 -d <container-id>`

To run in detach mode, *detach mode meaning it runs in the background*   
`docker run -p 4000:2000 -d 12345`

To start a stopped container in detach mode  
`docker start <container-id>`

To run in an interactive mode  
`docker run -p 4000:2000 -d -it <container-id>`

To run a container and have it removed when stopped  on port 4000 in detached mode  
`docker run -p 4000:2000 -d --rm 12345`

To run it back in an attached mode  
`docker attach <container-name>` OR `docker container attach <container-name>`

To start a stopped container in an attached mode  
`docker start -a <container-name>`


## Stopping Containers  

To stop a running container  
`docker stop <container-id>`

Alternatively,  
`docker exec -it <container-id> bash` then  
`kill 1`


## Removing containers  
> It is better to stop a container before removing it.

To remove a container  
`docker rm <container-id>`
N:B This removes only stopped container


To remove a list of containers  
`docker rm <container-name> <container2-name> <container3-name>`

To remove all containers  
`docker rm $(docker ps -aq)`

To remove running container  
`docker rm -f <container-id>`

To remove all running containers   
`docker rm -f $(docker ps -aq)`

To remove all Containers  
`docker container prune`


## Naming containers  

To name a container while creating from an Image  
`docker run --name <container-name> <image-name>`

## Removing Images  

To remove a single image , thid removes image not used by any container  
`docker rmi <image-name>` OR `docker image rm <image-id>`

To remove multiple images  
`docker rm <image-id> <image2-id>`

To remove all images  
> This removes all untagged images 
`docker image prune`

To remove all tagged and untagged images   
`docker image prune -a`

## Pulling images 

To pull images from the repository  
`docker pull <image-name>`

To pull from custom repositories  
`docker pull <repo-name/image-name>`

specifically, we can add the tag name  
`docker pull <ACCOUNT_NAME/REPO_NAME:TAG>`


## Tagging Images

To tag an image 
`docker build -t goals:latest .`

To rename an image tag  
> Note that this creates a clone of the image  
`docker tag OLD_NAME:TAG  NEW_NAME:TAG`


## Inspecting Images

To get the details of an image  
`docker image inspect <image-id>`


## To Get Container Logs 

To get the running log of a container  
`docker logs <container-name>`

To watch the logs   
`docker logs -f <container-name>`

To show the logs timestamps  
`docker logs -t <container-name>`

---

# Dockerfile  

> Docker build an Image from a docker file, to build an image you must create a Dockerfile in the base directory of the project and detail the configuration in the Dockerfile.

## Basic Configuration Verbs  

* **FROM**   
This is to outline the base image needed to build the current image


* **WORKDIR**  
This is the directory where the image file will be created

* **COPY**   
This copies the files from the file system to the image WORKDIR

* **RUN**  
  This run basic commands to build the image internally e.g npm install, mvn clean install.

* **EXPOSE**   
  This tells the port in the image to expose to the system's port

* **CMD**  
  This is the command that runs when the image has been built to make it run e.g npm start, mvn spring-boot:run 
  > But it should be in arrays of strings e.g ["npm", "start"]