# KUBERNETES CHEAT SHEET
## PODS
### Get all pods in the current namespace
```
Kubectl get pods
```

### Get pods in all namespaces
```
Kubectl get pods --all-namespaces
```

### Get pods with more details
```
Kubectl get pods -o wide
```

### Get the yaml for a pod
```
Kubectl get pod <pod> -o yaml
```

### Inspect a pod
```
Kubectl describe pods <pod>
```

### Get pods sorted by a metric
```
Kubectl get pods\
  --sort-by='.status.containerStatuses[O].restartCount'
```

### Get pods with their labels
```
Kubectl get pods --show-labels
```

### Get pods that match a label
```
Kubectl get pods -l <label>=<value>
```

### Forward traffic from a localhostt port to a pod port
```
Kubectl port-forward <pod. <localhost-port>:<pod-port>
```

## LOGS
### Show logs (stdout) of a pod
```
Kubectl logs <pod>
```

### Show logs (stdout) of pods that match a label
```
Kubectl logs -l <label>=<value>
```

### Show logs of previous installation of a container
```
Kubectl logs <pod> --previous
```

### Show logs for a specific container in a pod (i.e. init container)
```
Kubectl logs <pod>.c<container>
```

### Following logs from a pod
```
Kubectl logs -f<pod>
```

### Follow all logs from a pod that match a label
```
Kubectl logs -f-l <label>=<value> --all-containers
```

### Show logs with verbosity level of logs from 0-9
```
Kubectl logs <pod>--v=0:9
```

## DEPLOYMENT
### Get all deployments in the current namespace
```
Kubectl get deployment
```
