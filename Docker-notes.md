# Docker

## Installation
Install with [Homebrew](https://brew.sh/)
```
$ brew install docker docker-machine
```
--- 
#### After installation
```
$ docker-machine create main
$ eval $(docker-machine env main)
```
#### To list **_all running_** containers
```
$ docker ps
```
#### To list **_all_** containers
```
$ docker ps -a
```

#### Different ways to run a docker image in bash
```
$ docker run -i -t ubuntu bash
$ docker run -i -t ubuntu:16.04 bash
$ docker run -i -t [id] bash
```
If the ubuntu image is not available, docker will try and pull it from [docker-hub](https://hub.docker.com/)

---

###$ To run a Docker host.
```
$ docker-machine start [name of host] // i.e main
```
---
`docker run` creates a new conainer image everytime.

---

#### To restart Docker
```
$ docker start [container id]
$ docker attach [container id]
```

#### Commiting Docker changes
Example. After installing `wget` I want to save that installation
```
$ docker pull ubuntu
$ docker run ubuntu apt-get install wget
```
Get the container id
```
$ docker ps -l
```
Commit the change
```
$ docker commit [container id] iman/ping
```
The command
```
docker commit [OPTIONS] CONTAINER [REPOSITORY[:TAG]]
```
#### To run the container after commiting
```
$ docker run iman/ping
```
---
#### Save the container as a new image
```
$ docker commit [container id] new_image_name:tag_name
```
Verify it has been committed
```
$ docker images
$ docker run -i -t new_image_name:tag_name bash
```
This will take you inside the container.
```
$ which curl
```
This should return a file path

---
#### Deleting a container
```
$ docker rm [container name or id]
```
### Deleting an image
```
$ docker rmi [image name]
```



