# KUBERNETES CHEATSHEET
## KUBERNETES
- It is an open source platform for automating deployment and scaling of containers across 
clusters of hosts providing container centric infrastructure.

- It is a container orchestrator and can run Linux containers: 
   - Launch container.
   - Maintain and monitor container site.
   - Performs container - oriented networking.

## KEY CONCEPTS
- POD: These are the group of containers.

- LABELS: These are used to identify the pods

- KUBLELET: They are container agents, responsible for maintaining the set of pods.

- PROXY: They are the Load balancer for pods, helping in distributing tasks across the pods

- ETCD: A metadata service

- CADVISOR: For resource usage and performance stats.

- REPLICATION CONTROLLER: It manages pod replication.

- SCHEDULER: Used for pod scheduling in worker nodes.

- API SERVER: Kubernetes API server.

## KUBERNETES ARCHITECTURE
### MASTER
- It is responsible for maintaining the desired state for the cluster you are working on.
- "Master" indicates a set of processes that are used to manage the cluster.
- Contains info, API, scheduler, replication. controllers and master.

### WORKER NODES/ MINIONS
- Also called a minion. It contains the services necesssary to run the pods that are managed by the master.
- Some services include: Container runtime, Kubelet, Kube-proxy.
- Contains: Kubelet,cAvisor, Services, Pods and Containers.

## FEATURES
- AUTOMATED SCHEDULING: provides an advanced scheduler that helps launch conatiner on cluster nodes.

- SELF HEALING: reschedule, replace and restart dead containers.

- AUTOMATED ROLLOUTS AND ROLLBACKS: supports rollback bfor systems incase of a failure. 
  Enables rollout and rollback for the desired state.
  
- HORIZONTAL SCALING: can scale up and down the app as per required. 
  Can also be automated wrt CPU usage.
  
- SERVICE DISCOVERY AND LOAD BALANCING: uses unique IP and DNS name to containers. 
  This helps to identify them across different containers.

## PODS AND CONTAINER INTROSPECTION
| COMMANDS | FUNCTIONS |
| :--- | :--- |
| Kubectl get pods | Lista all current pods |
| Kubectl describe pod<name> | Describes the pod name |
| Kubectl get rc | List all replication controllers |
| Kubectl get rc -- namespace="namespace" | Lists all current pods |
| Kubectl describe rc<name> | Shoes the replication controller name |
| Kubectl get cvc | Lists the services |
| Kubectl describe svc<name> | Shows the service name |
| Kubectl delete pod<name> | Deletes the pod |
| Kubectl get nodes -w | Watch nodes continously |
  
## DEBUGGING
| COMMANDS | FUNCTIONS |
| :--- | :--- |
| Execute command on service by selecting conntainer | Kubectl exec<service><commands>[-c<$conatiner>] |
| Get logs from service for a container | Kubectl logs -f<name>>[-c<$container>] |
| Watch the kubelet logs | Watch -n 2 cat/var/log/kublet.log |
| Show metrics for node | Kubectl top node |
| Show metrics for pods | Kubectl top pod |
  
## OBJECTS
| ALL | CLUSTERROLEBLINDINGS | FUNCTIONS |
| :--- | :--- | :--- |
| cm= conf gmaps c | controllerrevisions | crd=custom respource definition |
| Cronjobs | cs= component status | csr= certificate signing requests |
| Deploy=deloyments | ds=daemon sets | ep= end points |
| ev= events | hpa= autoscaling | ing=ingress |
| jobs | limits=limit ranges | Netpol= Network policies |
| No= nodes | ns=namespaces | pdb=pod |
| po= pods | Pod preset | pod templates |
| Psp= pod security policies | Pv= Persistent volumes | pvc= Persistent volume claims |
| quota= resource quotas | rc= replication controllers | Role bindings |
| roles | rs= replica sets | sa= service account |
| sc= storage classes | secrets | sts= stateful sets |
  
## CLUSTER INTROSPECTION
| COMMANDS | FUNCTIONS |
| :--- | :--- |
| Get version information | Kubectl version | 
| Get cluster information | Kubectl cluster-info |
| Get the configuration | Kubectl config g view |
| Output info about a node | Kubectl describe node<node> |
   
## OTHER QUICK COMMANDS 
### Launch a pod with a name an image:
```
   Kubectl run<name> --image=<image-name>
```
   
### Create a service in <manifest.yaml>:
```
   Kubectl create -f<manifest.yaml>
```
   
### Scale replication counter to count the number of instances:
```
   Kubectl scale --replicas=<count>
```
   
### Map external port to internal replication port:
```
   Expose rc<name> --port=<external>--target-port=<internal>
```
   
### To stop all pod in <n>:
```
   Kubectl drain<n>--delete-local-data--force--ignore-daemonset
```
   
### Allow master nodes to run pods:
```
   Kubectltaintnodes --all-noderole.kuernetes.io/master-
```
