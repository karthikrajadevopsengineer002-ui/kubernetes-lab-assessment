# Kubernetes Lab Assessment

## Overview
This project contains the Kubernetes lab assessment implementation using Minikube, kubectl, and Nginx.

## Tasks Completed

### 1. Minikube and kubectl
- Installed and configured Minikube.
- Started Minikube using Docker driver.
- Verified kubectl connectivity.

### 2. Namespace and Nginx Deployment
- Created namespace: `k8s-assessment`
- Created Nginx Deployment: `nginx-deployment`
- Configured 3 replicas.

### 3. Nginx Service
- Created NodePort Service: `nginx-service`
- Service port: `80`
- NodePort: `30080`

### 4. ConfigMap and Secret
- Created ConfigMap: `nginx-config`
- Created Secret: `nginx-secret`
- Used ConfigMap and Secret values in the Nginx Deployment.

### 5. Persistent Storage
- Created PersistentVolume: `nginx-pv`
- Created PersistentVolumeClaim: `nginx-pvc`
- Mounted persistent storage to the Nginx container.
- Verified data persistence after pod restart.

### 6. Scaling
- Scaled Nginx Deployment from 2 to 3 replicas.
- Verified all 3 pods are running.

### 7. Rolling Update and Rollback
- Performed rolling update to Nginx `1.27`.
- Verified rollout successfully.
- Performed rollback to the previous Nginx image.

### 8. Verification
The following Kubernetes resources were verified:

- Pods
- Deployment
- Service
- ConfigMap
- Secret
- PersistentVolume
- PersistentVolumeClaim

## Kubernetes Resources

| Resource | Name |
|---|---|
| Namespace | k8s-assessment |
| Deployment | nginx-deployment |
| Service | nginx-service |
| ConfigMap | nginx-config |
| Secret | nginx-secret |
| PersistentVolume | nginx-pv |
| PersistentVolumeClaim | nginx-pvc |

## Verification Commands

```bash
kubectl get pods -n k8s-assessment
kubectl get deployments -n k8s-assessment
kubectl get svc -n k8s-assessment
kubectl get configmap -n k8s-assessment
kubectl get pv
kubectl get pvc -n k8s-assessment
