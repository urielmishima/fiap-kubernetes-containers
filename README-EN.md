# MediaWiki on Kubernetes

This project provides a deployment of MediaWiki on a Kubernetes cluster. The project uses a Deployment to deploy two copies of a MediaWiki container. The Deployment also uses probes to ensure that the containers are running and ready to receive requests. The Service exposes the Deployment to the outside world using a LoadBalancer.

## Prerequisites

To use this project, you need to have the following:

* A Kubernetes cluster
* The kubectl CLI installed and configured to connect to your cluster

## Deployment

To deploy this project, you can use the following command:

```
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

To get the load balancer IP address, you can use the following command:

```
kubectl get service mediawiki-service
```

The load balancer IP address is the value listed for `EXTERNAL-IP`.

## Files

* `deployment.yaml` - The deployment file that defines the Deployment for MediaWiki.
* `service.yaml` - The service file that defines the Service that exposes the Deployment to the outside world.

## Configuration

You can configure the project by modifying the `deployment.yaml` and `service.yaml` files. For example, you can modify the number of replicas in the Deployment or the Service type.

## Information

* **Course:** MBA in Cloud - Engineering & Architecture
* **Class:** 2CLDR
* **Name:** Uriel Mishima
* **RM:** 346005
* **Discipline:** Kubernetes Orchestration and Containers