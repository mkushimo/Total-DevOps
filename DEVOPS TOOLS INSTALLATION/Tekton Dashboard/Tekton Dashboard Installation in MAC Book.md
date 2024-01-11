# Install Tekton Dashboard  in MAC Book

To Install Tekton Dashboard first we need to create a cluster. To create a cluster we can kind tool.
Kind is a tool for running local Kubernetes clusters using Docker container “nodes”.

To install a kind, first we should install docker in our laptop.


To install kind in MAC book follow the below command.
```
#brew install kind
```

To check the version
```
#kind version
```

To Create a Kubernetes cluster use the below commands
```
#kind create cluster --name tektondemo : It will create a cluster with name 'tektondemo'
```

Deleting a Cluster 
```
##kind delete cluster --name tektondemo 
```

To display the nodes
```
#kubectl get nodes
```

To Display all the pods.
```
#kubectl get pod -A 
```

To create a namespace with the name 'tekton-pipelines'
```
#kubectl create ns tekton-pipelines
```

To install the latest version of  Tekton Dashboard.
```
#kubectl apply --filename https://storage.googleapis.com/tekton-releases/dashboard/latest/tekton-dashboard-release.yaml 

#kubectl apply --filename https://github.com/tektoncd/pipeline/releases/download/v0.16.1/release.notags.yaml

#kubectl get pods --namespace tekton-pipelines --watch
```
Note: Hit CTRL+C to stop monitoring.
```
#kubectl get all -n tekton-pipelines
```

## Accessing the Dashboard

### By using  kubectl port-forward
```
#kubectl --namespace tekton-pipelines port-forward svc/tekton-dashboard 9097:9097
```
Install Pipeline
----------------
Tekton Dashboard requires to have Tekton Pipelines installed.

Installing the latest Tekton Pipelines release is done by running the following command:
```
#kubectl apply --filename https://storage.googleapis.com/tekton-releases/pipeline/latest/release.yaml
```

Uninstalling the Dashboard on Kubernetes
```
kubectl delete --filename https://storage.googleapis.com/tekton-releases/dashboard/latest/tekton-dashboard-release.yaml
```

Tekton Dashboard extensions
---------------------------
Follow below url for Extensions 
https://github.com/tektoncd/dashboard/blob/main/docs/extensions.md
