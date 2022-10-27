# Kubernetes

## What is Kubernetes?

It is a container orchestration tool that automates container management, deployment and scaling. 

## What is a Kubernetes Cluster?

It is a set of nodes that run containerised applications.

## Basic Kubernetes Commands:

- `kubectl get svc`- lists all services
- `kubectl get pods`- lists all pods in the namespace
- `kubectl get deployments`- lists all the deployments in the namespace
- `kubectl create -f yamlfilename`- creates yamlfile
- `kubectl apply -f yamlfilename`- applies yamlfile
- `kubectl delete pod podname`- will create replica to ensure number
- `kubectl describe svc svcname`- 