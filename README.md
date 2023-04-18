# Deploying Application on Kubernetes and setup volumes

This guide explains how to deploy the sample application on a Kubernetes cluster using volume.

## Prerequisites

Before you get started, you need to have the following tools installed:

- Docker
- minikube or a Kubernetes cluster
- kubectl

## Building the app image

Navigate to the root directory of the cloned repository:

Build the Docker image and push it to a registry:

```bash
docker build -t leonlogli/kubernates-app-volume .
docker push leonlogli/kubernates-app-volume
```

Apply deployment and service

```bash
kubectl apply -f="kubernates.yaml"
```

Get the external IP address of the service:

```bash
minikube service kubernates-app-volume
```

Delete services and deployment

```bash
kubectl delete -f="kubernates.yaml"
```
