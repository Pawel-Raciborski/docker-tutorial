# Container and Network Requests

Two kinds of communication:
- Requests from container to WWW
- Requests from container to host machine(database etc.)
- Requests from container to other container

In docker the best practise is - one container - one thing to do

Communication between containers - cros communication

To connect to Host machine we use special type of host address:
'mongodb://host.docker.internal:27017/swfavorites'

Where _host.docker.internal_ is that special domain address

---


## First approach to communicate with containers

If we want use some another container we need to know its address - this is first approach - we know address then we assign that address to connection URL.


## Second approach to communicate with containers

Here we creating **Container Networks** where all containers can communicate with each other and IPs are automatically resolved

If more than one container are in the same network, they can talk to each other

1. First we need to create network.
2. Then we add containers to the same network (we use **--network _network-name_** flag)