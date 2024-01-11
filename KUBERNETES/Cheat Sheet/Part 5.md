# KUBERNETES PODS
- Pods are a group of containers represented for deployable obhects in Kubernetes. 
- A Pod could contain one or more containers (applications), one for the main process and the others to "support it".


### Get the documentation for Pod manifests
```
Kubectl explain pods
```

### A basic Pod manifest basic-pod-manifest.yaml
```
y basic-pod-manifest.yaml
apiVersion: v1
kind: Pod
metadata:
 name: static-web
 labels: 
  role: myrole
spec:
 containers:
 - name: web
   image: nginx
   ports:
   - containerPort: 80
     protocol: TCP
```

### Creating pods based in YAML file
```
Kubectl create -f basic-pod-manifest.yaml
```

### Get the YAML file of the Pod just created
```
Kubectl get pod nginx -o yaml
```

### List Pods and their state in the default Nmaespace
```
Kubectl get pods
```

### Get the definition of the Pod into a file
```
Kubectl get pod static-web.o yaml > manifest.yml
```

### List all the Pods in all Namespaces
```
Kubectl get pods --all-namespaces
```

### List Pods in a particular Namespace
```
Kubectl get pods --namespace=dev
```

### Delete a Pod
```
Kubectl delete pod nginx
```

### Delete a pod force
```
Kubectl delete pod nginx --force
```

### Show more details about a single Pod
```
Kubectl decribe pod static-web
```

### Create a Pod using imperative commands
```
Kubectl run nginx --image nginx
```

### Preview the object that would be sent to your cluster.
#### Don't create the Pod
```
Kubectl run nginx --imagenginx --dry-run=client -o yaml
```

#### Edit a Pod
```
Kubectl edit pod static-web
```

### Pod logs
```
Kubectl logs static-web -c web
```

### Pod port forwarding
```
Kubectl port-forwrd static-web 8884:80
```

### execute the simple shell on the pod
```
Kubectl exec -it static-web bash
```

### Connecting to the pod through the port forwarder
```
Kubectl localhost:8884
```
