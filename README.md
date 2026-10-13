Kubernetes Practice Lab

A hands-on Kubernetes project for learning and practicing core Kubernetes resources using YAML manifests, kubectl, VS Code, GitHub, and Killercoda.

Topics Covered
Pods
Deployments and replica scaling
ClusterIP Services
LoadBalancer Services
ConfigMaps
Secrets
Port forwarding
Rollout history and status
Troubleshooting Pods and Services
Prerequisites
A Kubernetes cluster or Killercoda Kubernetes playground
kubectl
Git and VS Code
Getting Started

Clone this repository and open the project directory:

git clone <YOUR_GITHUB_REPOSITORY_URL>
cd k8s-practice-lab


Apply the Pod manifest:

kubectl apply -f 01-pods/pod.yaml
kubectl get pods


Apply the Deployment and Service:

kubectl apply -f 02-deployments/deployment.yaml
kubectl apply -f 03-services/service.yaml
kubectl get deployments,services


Apply the practice configuration:

kubectl apply -f 04-configmaps-secrets/configmap.yaml
kubectl apply -f 04-configmaps-secrets/secret.yaml


Apply the LoadBalancer Service:

kubectl apply -f 05-loadbalancer/loadbalancer.yaml
kubectl get services


Note: A LoadBalancer Service requires suitable cluster infrastructure. In a local or training cluster, its external IP may remain pending.

Cleanup

Delete resources created during practice:

kubectl delete -f 05-loadbalancer/loadbalancer.yaml
kubectl delete -f 04-configmaps-secrets/secret.yaml
kubectl delete -f 04-configmaps-secrets/configmap.yaml
kubectl delete -f 03-services/service.yaml
kubectl delete -f 02-deployments/deployment.yaml
kubectl delete -f 01-pods/pod.yaml

Learning Goal

Practice writing YAML manifests, deploying resources, inspecting cluster state, and troubleshooting common Kubernetes problems.

This is a learning project. Demo credentials are not intended for production use.