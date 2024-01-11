# Kubernetes Cheat Sheet
## kubectl
```
   kubectl help      get help for kubectl
   kubectl version   get Kubernetes version running
   kubectl create    create a k8s object
   kubectl apply     create or update a k8s object
   kubectl get       get simple info on a k8s object
   kubectl describe  get detailed info on a k8s object
   kubectl config    used for kubeconfig settings
```

## Kubernetes Objects
```
   pod         deployment
   service     volume
   replicaset  daemonset
   job         namespace
   secret      configmap
```

## Creating and Deleting Kubernetes Objects
```
   kubectl apply –f manifest.yaml
   kubeclt apply –f ./dir
   kubectl create –f manifest.yaml
   kubectl apply –f https://alta3.com/test.yaml
   kubectl delete pod pod1
   kubectl delete –f manifest.yaml
```

## Kubernetes Manifest
```
   apiVersion: v1
   kind: Pod
   metadata:
      name: nginx
   spec:
   containers:
     - name: nginx
       image: nginx:1.7.9
       ports:
          - containerPort: 80
```

## get and describe Kubernetes Objects
```
   kubectl get services –namespace=namespace1
   kubectl describe deployment deployment1
   kubectl get pods –all namespaces
   kubectl describe nodes node1
   kubectl get pods pod1 –o yaml
   kubectl describe namespace default
```

## Context and Namespace
```
   kubectl config view
   kubectl config get-contexts
   kubectl config current-context
   kubectl config user-context mycontext
   kubectl create –f namespace-test.yaml
   kubectl get namespaces
```

## Logs and Debugging
```
         kubectl logs pod1
         kubectl get events
   --v=0      useful for operator visibility
   --v=1      good for default log levels
   --v=2      state information and important log messages relating to changes in the 
              system – recommended default log level for systems
   --v=3      more detailed information about changes
   --v=4      debug level
   --v=6      shows requested resources
   --v=7      includes HTTP request headers
   --v=8      includes HTTP request contents
   --v=9      shows HTTP request contents without truncation
```

