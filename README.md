# K8s Demo

A simple web app connected to MongoDB, deployed on Kubernetes.

## Files

- `mongo-secret.yaml` - Secret for MongoDB credentials
- `mongo-config.yaml` - ConfigMap with MongoDB service URL
- `mongo.yaml` - MongoDB Deployment and Service
- `webapp.yaml` - Web App Deployment and NodePort Service (port 30100)

## Run

```bash
kubectl apply -f mongo-secret.yaml
kubectl apply -f mongo-config.yaml
kubectl apply -f mongo.yaml
kubectl apply -f webapp.yaml
```

## Access (Minikube)

```bash
minikube service webapp-service
```

Keep the terminal open — minikube needs it for the tunnel on macOS.
