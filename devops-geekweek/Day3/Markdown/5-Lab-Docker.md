# Lab Docker


# Installing Docker
Prerequisites:
* Make sure you have a 64bit OS

On Windows:
* Windows 10: you may use Docker for windows (need to enable Hyper-V, beware this may interfere with Virtualbox in some setups)
* Windows 7: Use [Docker Toolbox](https://www.docker.com/toolbox) 

For both you have the option of installing a Linux VM and enable docker on that

#Docker info
First off we want to have a look at the Docker installation information, so run:

`docker info`

This should give you an output similar to this:

```
$ docker info
```

This command displays many information: how many images we have downloaded,  how many containers we have running, version of Docker etc.

#Launching your first container

Type:
```
docker run ubuntu /bin/echo 'Hello world'
```

* docker run runs a container
* ubuntu is the image (pulled from Docker Hub as this is the first time you used it)
* /bin/echo is the command that the container executes

#Docker ps

Docker ps displays running containers

Type:
```
docker ps
```

* Dos you see any container running
* Why?


#Launch a demonized container
Let's start a container that will last longer

Type:
```
docker run -d ubuntu /bin/sh -c "while true; do echo hello world; sleep 1; done"
```


