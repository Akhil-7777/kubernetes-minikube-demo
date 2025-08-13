# Kubernetes Minikube Demo

This repository demonstrates setting up a local Kubernetes cluster using Minikube and deploying a simple Nginx application.

## Contents

- `deployment.yaml`: Kubernetes deployment configuration
- `service.yaml`: Kubernetes service configuration
- Screenshots of the working deployment

## Steps to Reproduce

1. Install Minikube and kubectl
2. Start Minikube: `minikube start`
3. Apply the deployment: `kubectl apply -f deployment.yaml`
4. Apply the service: `kubectl apply -f service.yaml`
5. Access the service: `minikube service nginx-service`
6. Scale up to 4 replicas: `kubectl scale deployment nginx-deployment --replicas=4`
7. Verify scaling: `kubectl get pods`  #Now you should see 4 pods instead of 2.
8. To get detailed information about a pod: `kubectl describe pod <pod-name>`
9. To view logs of a specific pod: `kubectl logs <pod-name>`

## Screenshots
<img width="890" height="90" alt="2" src="https://github.com/user-attachments/assets/70788b64-a038-4a4b-bb44-3dc3bb9d2969" />
*Output of `kubectl get pods` showing running containers*

<img width="1002" height="94" alt="1" src="https://github.com/user-attachments/assets/9fdfb80c-9ad7-475d-8f2e-0d55564eecc1" />
*Output of `kubectl get services` showing the exposed service*



![Browser View](screenshots/browser-view.png)
*Nginx welcome page accessed through the service*
