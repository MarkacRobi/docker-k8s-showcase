# Docker + Kubernetes showcase

This repository contains a showcase of dockerized microservice being deployed in a Kubernetes cluster.

## Prerequisites

- [Node.js](https://nodejs.org/en/)
- [Docker Desktop](https://www.docker.com/products/docker-desktop) freely available in a community edition
- [Kubernetes](https://docs.docker.com/desktop/kubernetes/) included in Docker Desktop (must be enabled through settings)
- [Kompose](https://kubernetes.io/docs/tasks/configure-pod-container/translate-compose-kubernetes/) to translate a Docker Compose File to Kubernetes Resources

## How to

First clone the repository:

```sh
git clone https://github.com/MarkacRobi/docker-k8s-showcase.git
```

Install dependencies

```sh
npm install
```

Convert Docker Compose file in to k8s resources

```sh
kompose convert
```

Deploy resources in k8s cluster

```sh
kubectl apply -f api-service.yaml,api-deployment.yaml
```

Checkout the deployed resource information

```sh
kubectl describe svc api
```
