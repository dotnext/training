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

* Do you see any container running
* Why?


#Launch a demonized container
Let's start a container that will last longer

Type:
```
docker run -d ubuntu /bin/sh -c "while true; do echo hello world; sleep 1; done"
```

* Test to seee if the container is running with docker ps
* Examine its logs using the command 'docker logs' (you'll need its name..)
* Kill the container with 'docker stop' (you'll need its name..)

#Operating inside a container

Type:
```
docker run -i -t ubuntu /bin/bash
```

* Has your shell changed?
* what outputs do you get with ls -la or ifconfig?

`CTRL-d` exits the shell and shuts down the container. If you want to detach from it (while keeping the container running but ) use `CTRL-p CTRL-q`


#Build your own Container with a Dockerfile

A Dockerfile is  a simple textfile that describes a container:
* Where to start from (a linux distribution usually) **FROM**
* Commands to run to customize it (installing packages and/or editing configuration files) **RUN**
* Network port to use **EXPOSE**
* What to run **CMD**

DockerFile example

```
FROM ubuntu:12.04

MAINTAINER Kimbro Staken version: 0.1

ADD ./mysql-setup.sh /tmp/mysql-setup.sh
RUN /bin/sh /tmp/mysql-setup.sh

# Adding this will expose mysql on a random host port. It's recommended to avoid this. Other containers on the same 
# host can use the service without it.
#EXPOSE 3306

CMD ["/usr/sbin/mysqld"]
```
