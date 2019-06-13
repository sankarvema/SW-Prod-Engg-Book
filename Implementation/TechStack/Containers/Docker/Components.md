# Docker Components

- docker-compose: Command used to configure and manage a group of related containers. It is a frontend to the same api's used by the docker cli, so you can reproduce it's behavior with commands like docker run.
- docker-compose.yml: Definition file for a group of containers, used by docker-compose and now also by swarm mode.
- swarm mode: Used to manage a group of docker engines as a single entity and provide orchestration (constantly trying to correct any differences between the current state and the target state).
- service: One or more containers for the same image and configuration within swarm, multiple containers provide scalability.
- stack: One or more services within a swarm, these may be defined using a DAB or a docker-compose.yml file.
- bridge network: Network managed by a single docker engine where multiple containers may communicate with each other. You may have multiple networks managed by an engine, and containers can be attached to zero or more networks.
- overlay network: Similar to a bridge network but spanning multiple docker engines. These require a key/value store to maintain their state. Swarm mode provides this, but if swarm mode is disabled, you may also use etcd, consul, or zookeeper.
- links: a method to connect containers together that predates the bridged network. Its usage is no longer recommended.
- classic swarm: A predecessor to the integrated swarm mode that runs as a container, allows multiple engines to appear as one, but does not provide orchestration or include its own k/v store.


## Relating the Components

1. Docker image is a configuration and script defining a runnable
2. Docker container is a docker image running. Image run under docker engine
2a. Docker compose can be used to run such containers with single command based on the configuration in docker-compose.yaml
3. Set of such containers of the same image forms a service
3a. One of more services with in a swarm will become a stack, can be defined through DAB or docker-compose.yaml
4. One or more services will form swarm, running and orchestrated as a single entity
