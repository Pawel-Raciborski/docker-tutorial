## What is Docker?

It's platform that allows build, test and deploy applications quickly.

Docker packages software into _containers_ that got everything the software need to run(libs, code, runtime).

_container_ - is loosely isolated environment, possible to share between different OS


## Docker architecture

![Docker architecture](../assets/images/docker_architecture.png)


- it uses client-server architecture
- *Client(docker)* talks to the *Docker deamon*, *Docker deamon(dockerd)* listens for Docker API requests
- *Docker deamon* is responsible for building, running and disturbing Docker containers
- Docker client and Docker deamon can run on the same system, or we can connect Docker client to remote Docker deamon
- *Docker registry* stores Docker images. [Docker Hub](https://hub.docker.com/) is example of public registry, we can also use private registry

images, containers, networks, volumes, plugins, and other objects