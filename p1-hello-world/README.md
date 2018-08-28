#Docker Introduction
A quick and simple introduction into the world of docker.

##Overview 
* Images
* Dockerfile
* Compose Files


## Commands
A quick over view of the commands used in docker
* pull
* images
* run
* ps
* logs
* stop

## pull
Will pull the docker image hello-world
```bash
docker pull hello-world
```
![Pulling hello world](images/hw1.PNG)

## images
View images
```bash
docker images 
```
![Images view](images/hw2.PNG)

## run
Will pull the image, create a container and start it up. The last arg is the image name 

common args
* --rm: will remove the container once it has been stopped.
* -d: will run it detached mode or in the background.
* --name: give the container a name making it easier to manage.
* -it: interactive shell such as bash, etc.
* -p: setup ports example -p 3030:8080 what this is doing is mapping the port 8080 inside the container to the port 3030 outside of the container.
* --network: assigns the container to a specific network


EXAMPLE

![run view](images/hw3.PNG)

The long string of characters below the command is the ID of the container.

An example of the other args will be used later

## ps
common args
* -a: show all containers running and not running

This will show only the containers running

```bash
docker ps
```

![ps view](images/hw4.PNG)

#

This will show all of the containers running and stopped.

```bash
docker ps -a
```

![ps view](images/hw5.PNG)

## logs
Logs will print the the standard out from the container to the terminal
```bash
docker logs example
```
![ps view](images/hw6.PNG)

## stop
```bash
docker stop example
```
![ps view](images/hw7.PNG)

*This is not going to do much since the container stops after it runs.*

####This concludes the Introduction to docker.
