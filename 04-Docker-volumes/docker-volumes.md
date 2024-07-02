# Different kinds of Data

- Application (Code + Environment) - stored in Images
- Temporary App Data(entered user input) - stored in containers
- Permanent App Data(user accounts) - stored with Containers & Volumes

Volumes helps us with solving problem of storing data


# What are Volumes
Volumes are **folders on your host machine** hard drive which are **mounted("made available") into containers**

# Two types of External Data Storages
- Volumes(Managed by Docker)
    - Anonymous volumes - exists as long our container exists
    - Named volumes - are not removed when container is removed
- Bind Mounts(Managed by you)

Anonymous volumes are removed automatically if we add flag _--rm_ when we start / run a container. If we won't add that flag - anonymous volume would not be removed.
If we start again new container it will create new volume, the old one wouldn't be used.

_docker volume rm VOLUME-NAME_ - to remove volume with name


### Bind Mounts

You define folder / path on your local host machine

Binding example:
-v absolute_path:/docker_path
-v ${pwd}:/app


**By default Volumes are Read-Write**

Read-Only Volumes:


# Arguments and Environment Variables

### ARG:

Available inside of Dockerfile, NOT accesible in CMD

### ENV:

Available inisde of Dockerfile and in application code