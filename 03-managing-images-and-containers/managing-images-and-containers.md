_docker run_ - creates new container based on image

# Attached and Detached Containers

attached - docker running in the foreground(by default with _docker run_ command)
detached - docker running in the background(example _docker start_ method)

To run container in detach mode when using command _docker run_ add **-d** flag: _docker run -p 8000:80 **-d** 123vfdvn34o23_

_docker attach [container]_ - running container in attached mode


# Docker interactive mode
We can run container in interactive mode using with command: _docker run -it cca812e1b078757662b459d7ac17541d37995685b250a0a14b9040c8c7634f8f_

_docker container prune_ - to remove all stopped containers

If some container uses some image, we cannot remove that image until we not remove container which using that image

_docker inspect (imageid)_ - command for inspect image information

### Adding sth to container
_docker cp_ - copy files into running container or out the running container

_docker cp [path1] [path2]_ - copy file to a container

**path1**, **path2** - local host path or container file path to copy

_docker cp_ is not good idea to copy source code - it can invoke some problems


# Naming and tagging images and containers

## Image tags

name(repository):tag

name - is a group of images
tag - specialized version of image

---

# Sharing images

We can share images by:
- Sharing Dockerfile
- Share a Built Image(using DockerHub for example - typically this is used)

We can share images on:
- DockerHub
- Private Registory

_docker push IMAGENAME_ - used to share image
_docker pull IMAGENAME_ - used to use image

If repository is private instead of _IMAGENAME_ needs to be ***HOST:NAME***

### Publish Docker Image

First we need to create image with same name as described in command of docker repository. Then we can use _docker push [IMAGENAME]_ to push our image. Docker might not succesfully push our image - we need to log in.

