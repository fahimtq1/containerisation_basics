# Microservices Architecture

## What is Microservices Architecture?

It is a type of software architecture in which the software product is composed of small independent services that are able to communicate over well-defined APIs. Each service focus on an individual problem, so the code of one service doesn't need to be shared with another; making the application decoupled. Typically, each service will be allocated its own dedicated team.

### What are the Benefits?

- Easier deployment- as a consequence of each service being developed and tested by cross-functional teams, the troubleshooting of that service is more efficient
- Flexible scaling- adding or taking away functionality from the overall application is a much simpler process, as it equated to adding or taking away a service
- Application resilience- the application is not dependent on all of its components to run; the application is decentralised

## What is Containerisation?

It is the process of allocating an entire software component, including its environment, dependencies and configuration, into an isolated unit- AKA a container. Containers, that package the components of an application, all use the same operating system.

### What are the Benefits?

- Portability- a container bundles all the dependencies, so an application can be taken and deployed anywhere
- Faster delivery- containerisation compartmentalises your application, so it is easier to upgrade
- Improved security- due to the containers being isolated, if the security of one container is compromised, the other containers remain secure

## Project brief

The goal of the project is to gain an understanding of containerisation with Docker and implement that understanding by deploying an application using containers. A microservices architecture will be utilised with each service in its own container. 

### Main Docker concepts 

- Docker commands
- Dockerfile
- Docker compose YAML files