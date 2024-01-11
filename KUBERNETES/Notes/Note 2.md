# Kubernetes Glossary
## Containers and Container Orchestration
- Container: a lightweight and executable package of software that bundles application
  code together with all of the related configuration files, container runtimes, libraries,
  and dependencies required for it to run. Containers decouple applications from their
  underlying host environment making deployment easier in different environments.
  
- Container Image: an unchangeable, static file that contains everything required to run 
  an application, including the code, runtime, libraries, and more.
  
- Container Orchestration: automates many of the operational tasks required
  to run containerized applications, such as provisioning, deployment,
  management, scaling, networking, load balancing, and more.
  
- Container Orchestration Tools: software that creates, manages, and orchestrates containerized
  applications. Kubernetes is a popular, open-source container orchestration tool.
  
- Docker: a popular, open-source container software that can be used in conjunction with Kubernetes.

## Kubernetes Architecture
- Kubernetes Cluster: a working Kubernetes deployment that allows containerized applications
  to run across multiple environments, such as virtual, physical, cloud-based, and on-premise.
  The native Kubernetes cluster consists of master components that represent the cluster’s
  control plane and worker nodes that run containers and maintain the runtime environment.
  
- Kubernetes Control Plane: the controller for the Kubernetes cluster. It’s responsible for
  managing activities that affect the cluster as a whole, such as scheduling and scaling
  applications, maintaining a cluster’s state, and implementing updates. The control plane
  components include kube-api server, etcd, kube-scheduler, and kube-controller-manager.
  
   - kube-api server: lets you query and control the state of Kubernetes objects, such as Pods,
     Namespaces, and ConfigMaps. The core of the Kubernetes control plane is the API server and the
     Kubernetes Application Programming Interface (API) that it exposes. End users, different parts of
     your cluster, and external components can communicate with each other through the API server.
  
   - etcd: provides a highly-available, consistent, shared key value store for all Kubernetes cluster data.

   - kube-scheduler: monitors the cluster to detect newly-created pods that have no node assigned,
     and assigns it to a node for execution based on individual and collective resource requirements,
     hardware/software/policy constricts, affinity and anti-affinity specifications, locality, inter-workload
     interference, and deadlines.
     
   - kube controller-manager: manages the collection of individual controller processes as a single binary process. 
     The controllers include a node controller, a replication controller, an endpoints controller, a service account 
     and token controller, and cloud-controllermanager. Each controller manages a particular aspect of the cluster’s 
     current state and works to move the application from its current state towards the desired state.
      - Kubernetes Controllers: a non-terminating control loop that manages components and workloads. Each controller 
        manages a particular aspect of the cluster’s current state and works to move the application from its current 
        state towards the desire.
        
- Kubernetes Nodes: the physical servers or virtual machines in a Kubernetes
  cluster. The worker nodes perform the tasks assigned by the control plane, maintain
  running pods, and provide the runtime environment for the cluster. The components
  of a node include the kubelet, a container runtime, and the kube-proxy.
    - kubelet: an agent that runs on each node in the cluster to ensure that the containers
      created by Kubernetes for a pod are running and in a healthy state.
    - Container Runtime: responsible for running containers and supports several
      container runtimes, such as Docker or containerd, that runs on the cluster.
    - kube-proxy: serves as a network proxy that runs on each node in the cluster
      to enforce network routing and connection forwarding rules.       
        
## Kubernetes API
- Kubenetes API: enables Kubernetes to function. When you input information
  about the desired state of a cluster to the API, it passes the information to the
  Kubernetes control plane. The control plane instructs the worker nodes to carry out
  tasks that move the application from its current state to its desired state.
  
- Kubectl: a Kubernetes command line interface tool used to communicate with the API. Use
  the command line [?] to create, change, inspect, replicate, and destroy Kubernetes objects.
  
- Kubernetes Aggregation Layer:  allows Kubernetes to be extended with additional APIs, beyond
  what is offered by the core Kubernetes APIs. It runs in-process with the kube-api server.  
  
## Kubernetes Objects
- Kubernetes Objects: represents the state of your Kubernetes cluster by telling
  Kubetnetes what you want the workload to look like. Specifically, they can describe
  what containerized applications are running (and on which nodes), policies for using
  those applications, and the resources available to those applications.
  
    - Kubernetes Names: unique identifiers for Kubernetes objects that are client provided. Names refer
      to an object in a resource URL and only one object can have a specific name at any given time.
      
    - Kubernetes UIDs: Unique Identifiers (UID) for Kubernetes objects that are system-generated.
      Every object created over the lifetime of a Kubernetes cluster has its own UID.
      
    - Kubernetes Namespaces: a set of names that are used to easily identify and refer to a given
      set of Kubernetes objects. Namespaces can be used to divide cluster resources between
      multiple users (via resource quota), enhance Role-Based Access Controls (RBAC), create
      isolation between projects, teams, and different stages of an application’s lifecycle.
      
    - Kubernetes Labels: key-value pairs which are used to include non-identifying
      metadata which can be used to organize and select subsets of objects.
      
    - Kubernetes Selectors: used to query Kubernetes resources and filter them by their labels.
    
    - Kubernetes Annotations: key-value pairs which are used to include non-identifying data that
      will help people or other tools, but not Kubernetes directly. The metadata in an annotation can be
      structured or unstructured, small or large, and can include characters not permitted by labels.
      
## Kubernetes Workloads and Applications
- Kubetnetes Workloads: an application running on Kubernetes. A workload can be a single
  component or several that work together. You run a workload inside a set of pods.
  
- Kubernetes Pods: the smallest execution unit in a Kubernetes cluster that holds one or more
  containers that operate together. A pod contains storage resources, application containers,
  a unique network ID, and other configurations that are used to run a container.
  
- Kubernetes Workload Resources: manages a set of pods for you so you don’t have to manage each
  pod directly. Workload resources configure controllers to make sure the right number of the right
  kind of pods are running to match the cluster’s desired state. Kubernetes provides several built-in
  workload resources, such as Deployment, ReplicaSet, StatefulSet, DaemonSet, Job, and CronJob.
  
- Stateful: a process or application that saves data and keeps track of past sessions or transactions,
  such as setting preferences and recent activity. A majority of today’s applications are stateful.
  
- Stateless: a process or application that does not save data or have reference to past sessions
  or transactions. Each session or transaction acts as a single request or response.
  
- Kubernetes Operators: helps extend Kubernetes functionality for specific software and use cases.
  Operators take all of the knowledge about an application’s lifecycle and systematize it as code so that
  everything that can be automated is done so in a scalable, repeatable, and standardized manner.
  
## Kubernetes Configuration
- ConfigMaps: an API object used to store non-confidential data in Kubernetes,
  such as connection strings, public credentials, hostnames, and URLs. Use a
  ConfigMap to keep your application code separate from your configuration.
  
- Kubernetes Secrets: an API object used to store confidential data in Kubernetes,
  such as a password, a token, or a key. Using a Secret means that you don’t
  have to hold confidential information in your application code.
  
## Kubernetes Policies
- Kubernetes Resource Quotas: provides constraints that can limit resource consumption
  and creation on a namespace basis in Kubernetes. Resource Quotas can limit the quantity
  of objects that can be created in a namespace by type, as well as the total amount of
  compute resources that can be consumed by resources in that namespace.
  
- Kubernetes Limit Ranges: provides constraints on resource allocations to Pods or
  Containers in a namespace in Kubernetes. Limit Ranges can enforce minimum and maximum
  compute resources and storage requests per Pod or Container in a namespace.
  
- Kubernetes Network Policies: allows you to control traffic flow at the IP address
  or port level for particular applications in your Kubernetes cluster.

## Kubernetes Authentication and Access
- Role-Based Access Control (RBAC): regulates access to Kubernetes cluster resources.
  This mechanism of authorization allows admins to configure access policies through the
  Kubernetes API that determine what users can and cannot do inside a cluster.
   - Roles: are the means by which you define authorization to perform actions on
     resources. Roles always set permissions within a particular namespace, meaning
     they can only define authorization within the namespace it belongs in.
     
   - ClusterRoles: are the means by which you define authorization to perform actions
     on resources. A ClusterRole is similar to a Role, except it is not namespaced.
     
   - Authorized Subjects: who or what can be assigned Roles and ClusterRoles.
   
   - RoleBindings: is used to assign roles and subjects to a particular namespace.
   
   - ClusterRoleBindings:  is used to assign roles and subjects to Kubernetes clusters.
   
- OpenID Connect (OIDC): is a user authentication method that allows admins to verify
  the identity of the end user based on the authentication performed by the authorization
  server. It also allows admins to request and receive information about authenticated
  sessions and end users. OIDC is an extension of the OAuth2 authentication protocol.
  
- Lightweight Directory Access Protocol (LDAP): is an open, vendor-neutral and cross platform
  protocol used for directory services authentication. LDAP sends messages, such as client
  requests or server responses to data formatting, between services and applications.
  
## Kubernetes Networking
- Cluster Networking: a model within Kubernetes that enables communication
  between different pods. Containers within a pod use networking to communicate
  via a shared filesystem or the loopback network interface, localhost.
  
- Container Network Interface (CNI):  defines a standard plugin interface for Linux
  container networking. CNI is responsible for the network connectivity of containers
  and removing allocated resources when the container is delated.
  
- Ingress:  an API object that allows external traffic to access the services in your Kubernetes cluster.

- Load Balancing: is the process of distributing network traffic across multiple
  servers to prevent any single server from getting overloads or breaking down.
  
- Service Discovery: the process of automatically locating applications and services on a network.

- Calico: a network overlay that governs the network communication
  within the cluster and supporting services.
  
- Traefik: an ingress controller for routing and load balancing traffic to services and applications.

- CoreDNS: ensures that complex DNS tasks are automated to
  ensure dynamic capabilities of service interactions. 
  
## Kubernetes Scheduling
- Kube-scheduler: makes sure that pods are matched to nodes so that Kubelet can run them.

- Affinity: an advanced scheduling feature in Kubernetes 1.6 that provides you with
  greater flexibility and control of how your nodes or pods are scheduled. 
  
## Kubernetes Monitoring
- Kubernetes Monitoring: a form of reporting that provides detailed information
  about an application’s resource usage by examining the containers, pods,
  services, and the characteristics of the overall cluster.
  
- Kubernetes Cluster Metrics: provides metrics on the capacity and
  resource utilization of your Kubernetes clusters.
  
- Kubernetes Control Plane Metrics: provides metrics to ensure the
  control plane is working properly and efficiently.
  
- Kubernetes Node Metrics: provides metrics on the CPU, memory capacity, and node network traffic.

- Kubernetes Pods and Container Metrics: provides metrics to
  ensure pods and containers are running optimally.
  
- Kubernetes Application Metrics: provides metrics, such as Request Rate, Error Rate, and Duration
  (RED), that can help you ensure Kubernetes services are working properly and efficiently.

- Prometheus: a service designed to provide real-time metrics as you
  monitor the usage of resources within a Kubernetes cluster.
  
- Grafana: a tool designed to work with Prometheus to provide a visual representation
  of performance and other metrics within the Kubernetes cluster.
  
- Telegraf: a technology for coordinating the collection of metrics and
  events from across the resources within a Kubernetes cluster.
  
- AlertManager: sends alerts so you can stay informed of all events occurring in your cluster.

## Kubernetes Logging
- Kubernetes Logging: collects and visualizes logs from Kubernetes, platform services,
  and applications deployed on the cluster, which can be very useful for debugging.
  
- Fluentbit: an open-source log processor and forwarder for collecting log and
  event information from across the resources in the Kubernetes cluster.
  
- Elasticsearch: a distributed search engine which empowers the ease of searching through
  log and event information as it is collected from all parts of the Kubernetes cluster.
  
- Kibana: a technology that empowers Eleasticsearch data to be visually represented and
  navigated so that operational roles may easily diagnose events or issues within a cluster.
  
## Kubernetes Storage
- Ephemeral Volumes: a type of storage that is cleaned up when the
  workload is deleted or the container crashes. It’s automatically managed
  by Kubernetes and typically does not require explicit settings.
  
- Persistent Volumes: are storage resources that can be used by the cluster. Persistent
  Volumes are volume plug-ins that have lifecycle capabilities that are independent
  of any Kubernetes pod or deployment. You may have stateful workloads requiring
  persistent storage whose lifecycle is longer than that of pods or containers.
  
## Kubernetes Scaling
- Cluster Autoscaling: automatically scales up capability when there is greater demand and
  scales down capability when it is not needed, which can significantly save on costs. 
