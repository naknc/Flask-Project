# Simple Flask Project on Kubernetes

This project demonstrates how to deploy a basic Flask web application on Kubernetes.

## Prerequisites

Before you begin, ensure you have the following prerequisites installed:

- Docker
- Kubernetes Cluster
- kubectl
- Git

## Getting Started

### Step 1: Clone the Repository

```
  git clone https://github.com/naknc/kubernetes-flask-project.git
  cd kubernetes-flask-project
```

### Step 2: Build and Push the Docker Image

```
docker build -t your-docker-username/flask-project:latest .
docker push your-docker-username/flask-project:latest
```
Replace your-docker-username with your Docker Hub username.

### Step 3: Deploy to Kubernetes
```
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```
### Step 4: Access the Application
Find the external IP for the service:

```
kubectl get svc flask-service
```
Open a web browser and go to http://<external-ip>/ to see the "Great Success" message.

## Cleanup

To remove the deployed resources:

```
kubectl delete -f service.yaml
kubectl delete -f deployment.yaml
```

## License

This project is under the MIT License. See LICENSE for details.

## Acknowledgments

Flask: Flask Web Framework
Kubernetes: Kubernetes Documentation


