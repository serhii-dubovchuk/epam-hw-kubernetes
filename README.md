# EPAM Module 2: Kubernetes. Homework

## Disclaimer
This homework has a MS Word explanatory document uploaded to the EPAM educational platform. Please refer to that document in the first place, as it has all steps described.

## Original Web App's repository
https://github.com/redis-developer/basic-redis-chat-app-demo-nodejs


## Prerequisites
1. the Minikube is needed: https://kubernetes.io/ru/docs/tasks/tools/install-minikube/
2. the Helm package manager is needed: https://helm.sh/docs/intro/install/
3. Docker is needed: https://www.docker.com/products/docker-desktop/
4. (Optional) JMeter: https://www.simplilearn.com/tutorials/jmeter-tutorial/jmeter-installation 

## Running the cluster
1. Execute `minikube start --driver=docker`

2. Navigate to the `./kubernetes` folder and perform this command:
```
kubectl apply -f .
```
2. Perform these commands in order to install the Prometheus and Metrics Server:
```
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts

helm repo update

helm install prometheus prometheus-community/kube-prometheus-stack

kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
```
