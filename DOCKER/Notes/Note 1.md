# INTRODUCTION TO DOCKER

Docker is a tool that allows you to create, deploy, and run applications by using containers. Using docker you can run your software on different systems and environments like a development environment, a production environment. And,  the software will run  consistently, regardless of what kind of environment it's on.


## DOCKER ARCHITECTURE

- Docker Client: The Docker client and daemon communicate using a REST API, over UNIX sockets or a network interface.
- Docker Daemon (dockerd): The Docker daemon (dockerd) listens for Docker API requests and manages Docker objects
- Docker Registries: A Docker registry stores Docker images.


## DOCKER INSTALLATION
### Docker CE Installation Commands: CentOS
- Step 1: Package Installation. sudoyum install -y yum-utils\device-mapper-persistent-data \lvm2
- Step 2: Add Docker CE Repo. sudoyum-config-manager \--add-repo \https://download.docker.com/linux/centos/docker-ce.repo
- Step 3: Install Docker CE packages.sudoyuminstalldocker-ce docker-ce-cli containerd.io
- Step 4: Start Docker Service.sudosystemctlstartdocker
- Step 5: Enable Docker Service. sudosystemctlenabledocker
- Step 6: Check Docker Version. sudodocker version
- Step 7: Add ‘user’ to ‘docker’ group.sudousermod-a –G docker <whoami>
- Step 8: Log-out & log-in. And, run “docker run” command. docker version docker runhello-worldReference
  
### Docker CE Installation Commands: Ubuntu
- Step 1: Package Installation. sudo apt-get update. sudo apt-get -y install \. apt-transport-https \. ca-certificates \. curl \. gnupg-agent \.software-             properties-common.
- Step 2: Add Docker GPG Key. curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -.
- Step 3: Add repository. sudo add-apt-repository \.  "deb [arch=amd64] https://download.docker.com/linux/ubuntu \. $(lsb_release -cs) \. stable".
- Step 4: Install Docker CE packages. sudo apt-get update. sudo apt-get install docker-ce docker-ce-cli containerd.io
- Step 5: Check Docker version. sudo docker version.
- Step 6: Add ‘user’ to ‘docker’ group. sudo usermod -a –G docker <whoami>
- Step 7: Log-out & log-in. And, run command. docker version. docker run hello-world.
  
## RUNNING CONTAINER
### Verify Installation
If I run ‘docker version’ command before adding ‘user’ to ‘docker’ group I get
permission denied error. Because user doesn’t have permission for ‘Docker
Commands’. Hence, we have to give permission to user by adding user to
‘docker’ group to access docker commands.
 
## Docker Basic Commands 1:
Instantiate a container using ‘docker container run’ command and learn options and flags associated with it.
```
- docker container run [OPTION1 OPTION2 … OPTIONn] [Image]:[TAG] [COMMAND] [ARGUMENT]
  IMAGE: Docker Image.
  TAG: Run specific version of an image.
  COMMAND: Command to run inside the container.
  ARGUMENT: Arguments for the COMMAND.
```
  
## Run Container:
```
- docker run hello-world
- docker container run hello-world (Recommended way)
- docker run nginx
- docker container run nginx (Recommended way)
```
### Run a container with COMMAND and ARGUMENT:
- docker run busybox echo Hello Students!
  - echo: Command run inside the busybox container.
  - Hello Students!: Argument for the Command.
### List all containers (Running and stopped):
- docker ps -a
    o -a: All
### Remove a stopped container:
- docker rm [Container ID]
  
## Docker Images and Containers
### Image:
An image is built up of series of layers and each layer represents an instruction in the image.
  
### Container layer:
When a container is created from an image it adds a new writable layer on top
of the image layers. This layer is called as "container layer".
  
The major difference between a container and an image is the top container layer.
The diagram shows multiple containers sharing the same Ubuntu image. When you create containers
from an image, the container and image become dependent on each other and you can't delete the image
until all the containers attached to that image have been deleted.
  
When the container is deleted, the container layer is also deleted.
However, the underlying imagen remains unchanged.
  
## Docker Basic Commands 2:
### Docker help:
```
- docker --help | more
  - Management commands.
   - Commands.
```
### Management Commands:
```
- containers: Manage containers
- docker container --help
  - run: Run a command in a new container.
  - ls: List containers.
  - rm: Remove one or more containers.
```
- image: Manage images
- network: Manage networks
- node: Manage Swarm nodes
  
### Run a Container with options:
```
- docker container run nginx
- docker container run -d --name mynginx nginx:1.17.9
    o -d (or) --detach: Detached/Background Mode.
    --name: Provide desired meaningful name.
```
### List running containers:
```
- docker container ls
```
### List all containers (Running and Stopped):
```
- docker container ls -a
```
### Remove a container:
```
- docker container rm [container ID]
```
  
### Publish Port(s):
```
There are 2 types:
- --publish (or) -p:
- --publish-all (or) -P:
```
#### --publish (or) -p:
Publish a container's port(s) to the host.
```
- docker container run -d --name [container name] -p [Host port]:[Container port] [Image]
  Example:
          - docker container run -d --name mynginx -p 8080:80 nginx
```
#### --publish-all (or) -P:
Publish all exposed ports to random ports.
```
- docker container run -d --name [container name] -P [Image]
  Example:
          - docker container run -d --name mynginx2 -P nginx
```

### Display detailed information of a container:
```
- docker container inspect [Container ID/Container name]
  Example:
          - docker container inspect mynginx
```
### List port mapping:
```
- docker container port [Container ID/Container name]
  Example:
          - Docker container port mynginx
  
```
  
### --interactive (or) -i and --tty (or) -t:
When you detach from the container it's going to stop the container.
--interactive (or) -i: Keep STDIN open even if not attached
--tty (or) -t: Allocate a pseudo-TTY
```
- docker container run --name [container name] -it [Image]
  Example:
          - docker container run --name myubuntu -it ubuntu
```
### attach:
Attach local standard input, output, and error streams to a running container.
When you detach from the container it's going to stop the container.
```
- docker container attach [Container name/Container ID]
  Example:
          - Docker container attach myubuntu
```
### exec:
Run a command in a running container.
exec will not stop the container when you detach from the running container.
```
- docker container exec [Options] [Container ID/Container name] [Command] [Arguments]
  Example:
          - docker container exec -it myubuntu /bin/bash
```

### Container Restart Policy:
Automatically start the containers when they exit, or when Docker restarts.
```
- docker container run [Options] --restart [restart policy] [Image]
- Types of restart policies:
   - no
   - on-failure
   - always
   - unless-stopped
```
### no:
Default restart policy.
Do not automatically restart the container.
```
Example:
- docker container run --restart no nginx
- docker container run nginx (Same as above)
```
### on-filure:
Restart the container if it exits due to an error (i.e. non-zero exit code)
```
Example:
        - docker container run --restart on-failure [Image]
```
### always:
Always restart the container if it stops. If it is manually stopped, it is restarted only when Docker daemon
restarts or the container itself is manually restarted.
```
Example:
        - docker container run -d --name mynginxAlways --restart always -p 8080:80 nginx
```
### unless-stopped:
Similar to always, except that when the container is stopped (manually or otherwise), it is not restarted even
after Docker daemon restarts.
```
Example:
        - docker container run -d --name mynginxUnless --restart unless-stopped -p 8081:80 nginx
```

### Container Basic Commands:
#### List running containers:
```
   - docker container ls (Recommended way)
   - docker ps
```
#### List all containers (Running and Stopped):
```
   - docker container ls -a (Recommended way)
   - docker ps -a
```
#### Stop a container:
```
   - docker container stop [container ID/Container name]
```
#### Start a container:
```
   - docker container start [container ID/Container name]
```
#### Pause a container:
```
   - docker container pause [container ID/Container name]
```
#### Unpause a container:
```
   - docker container unpause [container ID/Container name]  
```
#### Fetch the logs of a container:
```
   - docker container logs [Container name/Container ID]
```
#### To see container resource usage statistics
```
   - docker container stats [Container name/Container ID]
```
#### To see running processes of a container:
```
   - docker container top [container ID/Container name]
```
  
### Image Basic Commands:
#### Pull an image:
```
   - docker image pull [Image]
```
#### List images:
```
   - docker image ls
```
#### To see detailed information of an image:
```
   - docker image inspect [Image]
```

### Clean Up: Remove Images and Containers.
#### Remove a stopped container:
```
   - docker container rm [Container Name/Container ID]
```
#### Remove all stopped containers:
```
   - docker container prune
```
#### Remove a running container :
```
   - docker container rm -f [Container Name/Container ID]
```
#### Remove all stopped and running containers :
```
   - docker container rm -f `docker ps -a -q`
```
   - docker container rm –f `docker container ls -a -q`
#### Remove an image:
```
   - docker image rm [Image]
```
#### Automatically remove a container when it exits:
```
   - docker container run --rm [Image]
```
  
## UNINSTALL & UPGRADE DOCKER ENGINE
### Uninstall Docker Engine:
```
- sudo systemctl stop docker
- sudo apt-get remove -y docker-ce docker-ce-cli
- sudo apt-get update
```
### Install Docker Engine (Lower Version):
```
- sudo apt-get install -y docker-ce=5:18.09.4~3-0~ubuntu-bionic docker-ce-cli=5:18.09.4~3-0~ubuntubionic
```
### Check Docker Engine Version:
```
- docker version
```
### Upgrade Docker Engine:
```
- sudo apt-get install -y docker-ce=5:18.09.5~3-0~ubuntu-bionic docker-ce-cli=5:18.09.5~3-0~ubuntubionic
```
### Check Docker Engine Version:
```
- docker version
```
  
### Docker Swarm:
```
- Run containers on multiple servers as a cluster.
- Build distributed cluster of Docker machine.
- Supports orchestration, high-availability, Scaling, load balancing etc..
```
### Manager:
```
- Assign work to worker nodes.
- Responsible for controlling the cluster and orchestration.
```
### Workers:
```
- Responsible for running container workloads.
```
### Configure Swarm Manager:
```
- Install Docker CE. (Section 3: Chapter – 1/2).
- docker info | grep swarm
- docker swarm init --advertise-addr [Swarm Manager Private IP]
- docker info | grep swarm
- docker node ls
```
### Add worker Node to Swarm Manager:
```
- Install Docker CE. (Section 3: Chapter 1/2).
- docker swarm join-token worker (On Swarm Manager)
- Copy and run the swarm join-token output. (On Worker Node).
- docker node ls (On Swarm Manager)
```
  
## DOCKER IMAGES
### IMAGES:
Docker image is a file which contains dependencies, binaries and required configurations to run software
inside a container.
```
- docker pull [Image Name]:[tag]
- docker image pull [Image Name]:[tag] (Recommended way)
```
### List all layers of an image:
```
- docker image history nginx
```
  
## Dockerfile:
Dockerfile is a set of instructions and commands used to build an image.
### Build Image:
```
- docker image build -t [TAG] .
- docker image build -t [TAG] -f [Dockerfile Name] .
- docker image build --no-cache -t [TAG] .
```
### Key Points To Remember:
```
- Ephemeral container.
- Order of execution.
- Keep image size minimum.
   - Avoid unnecessary packages and files.
   - Use multi-stage build.
   -  Keep number of layers to minimum.
```
### Frequently used Dockerfile Instructions:
#### FROM
```
 Sets base/parent Image.
```
#### LABEL
```
 Adds metadata to the image.
```
#### RUN
```
 Creates new layer.
```
#### EXPOSE
```
 Intend port to publish.
```
#### CMD
```
 Setting default command for container. It can be overridden.
```
#### ENTRYPOINT
```
  Specify executable inside the container. It does not get overridden.
  However, it can be overridden by --entrypoint flag.
```
#### WORKDIR
```
  Sets current working directory.
```
#### COPY
```
  Copy file from one location to container.
  If spaces include quotes
```
### ADD
```
  Similar to ADD instruction with additional features.
  if spaces include quotes.
  Download a file from URL.
    - ADD http://<www.abcxyz.com>/downloads/file.zip
```
#### ENV
```
  Set environment variables.
  Can be overridden by --env flag.
  ENV [Key]=[Value]
```
#### USER
```
  Set user.
```
#### HEALTHCHECK
```
- Checks the health of a container by running a command inside the container.
- Can be only one Healthcheck instruction in a Dockerfile.
- Options for CMD:
  -  --interval=DURATION (default: 30s)
  - --timeout=DURATION (default: 30s)
  - --start-period=DURATION (default: 0s)
  - --retries=N (default: 3)
       HEALTHCHECK --interval=5s CMD curl localhost:<port>
```
#### ARG
```
  Declared before the FROM instruction.
```
  
## DOCKER IMAGE CLI
#### Pull an image:
```
  docker image pull nginx
  docker image ls
```
#### Search an Image:
```
  docker search nginx
```
#### Limit the number of result:
```
  docker search --limit 10 nginx
```
#### Filter search result:
```
  docker search --filter stars=200 nginx
  docker search -f stars=100 -f is-official=true nginx
```
#### List images:
```
  docker images
  Docker image ls
  Docker image ls –a
```
#### Tag an image:
```
  docker image tag [Source Image]:[tag] [Reference to source image]:[tag]
  docker tag ubuntu myubuntu:v1
```
#### Delete an image:
```
  docker image rm nginx
  docker rmi nginx
```
#### Remove dangling image:
```
  docker image prune
```
#### Remove all unused and dangling image:
```
  docker image prune -a
```
#### Inspect an image:
```
  docker image inspect nginx
  docker image inspect nginx - -format”{{.ContainerConfig.Hostname}}”
```
  
## Flattening an Image
### Execution steps:
```
Flattening an image to a single layer to save some space and get an extra performance.
```  
#### Flattening an Image:
- docker export
- docker import
- docker image history
  
### Multi-Stage Builds:
- Multi-stage builds will have more than one FROM instructions in the Dockerfile.
- Each FROM instruction creates a new build.
  
## SAVE AND LOAD AN IMAGE
### Save an Image:
Save one or more images to a tar archive.
```
  docker image save [image name] > [archive name].tar
```
### Load an Image:
Load an image from a tar archive or STDIN.
```
  docker image load < [archive name]
```

## PERSISTENT AND NON-PERSISTENT STORAGE
### Storage Driver:
- Provides temporary internal storage for containers.
- Manages and controls how images and containers are stored on your Docker host.
                              
### Docker Storage:
Store and manage container data.
### Two types of storage:
1. Non-Persistent
2. Persistent
#### Non-Persistent Storage:
- Data resides within the container
- Get deleted when container deleted
- All container has it by default.
##### Storage Drivers:
```
  RHEL/Latest Ubuntu & CentOS uses Overlay2
  Ubuntu 14 and older uses aufs
  CentOS 7 and older uses devicemapper
  Windows uses its own.
```
##### Storage Location:
```
  Linux: /var/lib/docker/[STORAGE-DRIVER]/
  Windows: C:\ProgramData\Docker\windowsfilter\
```

#### Persistent Storage:
- Data does not reside within the container
- Does not get deleted when container deleted
                              
#### Two types Persistent Storage:
##### Volumes:
```
  Mounted to a directory in a container.
```
  - Storage Location:
       Linux: /var/lib/docker/volumes/
       Windows: C:\ProgramData\Docker\volumes
  - Supports 3rd party drivers:
       Block Storage e.g. Amazon AWS EBS.
       File Storage e.g. Amazon AWS EFS.
       Object Storage e.g. Amazon AWS S3.
##### Bind Mounts:
```
 File or directory on the host system is mounted into a container’s file or directory.
```                             
                              
## DOCKER STORAGE - VOLUMES
```                              
Mounted to a directory in a container.
```                              
Volume CLI:
- Create a Volume.
```
  docker volume create [volume name]
```                     
- List Volumes.
```                              
  docker volume ls
```                              
- Inspect a Volume.
```                              
  docker volume inspect [volume name]
```                              
- Remove a volume.
```                              
  docker volume rm [volume name]
```                              
- Delete all unused volumes.
```                              
  docker volume prune
```                              

###  Two ways to mount volume into a container:
 1 - - mount
Syntax:
```                              
docker container run -d \
--name mynginx1 \
--mount type=volume,\
source=nginxvolume,\
target=/usr/share/nginx/html/ \
nginx
```                              
 2 - - volume or - v
Syntax:
```                              
docker container run -d \
--name mynginx2 \
-v nginxvolume:/usr/shared/nginx/html/ \
nginx
```                              

##  DOCKER STORAGE – BIND MOUNTS
```                             
File or directory on the host system is mounted into a container’s file or directory.
```                              
### Two ways to create Bind Mounts:
 1 - - mount
Syntax:
```
docker container run -d \
--name nginxbind1 \
--mount type=bind,\
source="$(pwd)"/bindexample,\
target=/app \
nginx
```                              
 2 - - volume or –v
Syntax:
```                              
docker container run -d \
--name nginxbind2 \
-v /user/username/bindexample2:/app \
nginx
```                              

## DOCKERFILE – VOLUME INSTRUCTION
```
Volume instruction automatically creates a volume and mounts that volume to specified directory.
```                              
### Dockerfile: 
```
## Sample Dockerfile
FROM nginx
Label Description="Using Volume Instruction"
Volume ["/usr/share/nginx/html/"]
```                              

## STORAGE DRIVER
-  Provides temporary internal storage for containers.
- Manages and controls how images and containers are stored on your Docker host. 
                              
### Check default Storage driver:
- docker info
- docker info | grep storage
                              
### Method -1 : Edit unit file (docker.service)
- Add --storage-driver flag
```                              
  sudo vi /lib/systemd/system/docker.service
  ExecStart=/usr/bin/dockerd --storage-driver devicemapper -H fd:// --
  containerd=/run/containerd/containerd.sock
```                              
- Restart the docker
```                              
  sudo systemctl daemon-reload
  sudo systemctl restart docker 
```
                              
### Method 2: Configuration file (daemon.json)
- Configure daemon file
```                              
  sudo vi /etc/docker/daemon.json
```                              
- Restart Docker
```                              
  sudo systemctl restart docker
  sudo systemctl status docker 
```
                              
##  INTRODUCTION TO DOCKER SWARM
###  Docker Swarm:
- Build distributed cluster of Docker machine. Cluster consists of one or more nodes.
- Run containers on multiple servers as a cluster.
- Supports orchestration, high-availability, Scaling, load balancing, rolling updates, rollbacks etc..
- Swarm uses mutual Transport Layer Security (TLS) for communication and authentication of nodes.
                              
### Two Types of Node in Swarm:
1. Manager
  - Assign work to worker nodes.
  - Responsible for controlling the cluster and orchestration.
2. Worker
 - Accepting tasks from the Manager node and running container workloads. 

                              
###  Docker Swarm Cluster:
```                              
Manager/s assign work to Worker node/s. And, Swarm uses mutual Transport Layer
Security (TLS) for communication.  
```                              

## DOCKER SWARM CONFIGURATION
###  Docker Swarm Set-up:
1. Configure Swarm Manager.
2. Add worker node to Swarm manager.
### Configure Swarm Manager:
- Install Docker CE. ( Section 3: Chapter – 1/2).
- docker info | grep Swarm
- docker swarm init --advertise-addr [Node Private IP]
- docker info | grep Swarm
- docker node ls
### Add worker Node to Swarm Manager:
- Install Docker CE. (Section 3: Chapter – 1/2).
- docker swarm join-token worker (On Swarm Manager)
- Copy and run the swarm join-token output (On Worker Node)
- docker node ls (On Swarm Manager) 
                              
## DOCKER SWARM AND NODE COMMANDS 
### Swarm and Node Commands:
- List all nodes. (On Manager)
```                              
   docker node ls
```                              
- To inspect a node
```                              
   docker node inspect [Node Id]
```                              
- Promote a node to Manager.
```                              
    docker node promote [Node Id]
```                              
- Demote a node to Worker
```                              
    docker node demote [Node Id]
```                              
- Remove a node from Swarm
  Step1: On Manager
```                              
         docker node rm -f [Node name]
```                             
Step 2: On Worker
```                              
         docker swarm leave
```                              
- Generate Join-token for worker. (On Manager).
```                              
  docker swarm join-token worker
```                              
- Generate join-token for manager. (On Manager).
```                              
  docker swarm join-token manager
```
                              
## DOCKER SWARM AUTOLOCK
### Docker Swarm:
- Encrypts RAFT logs and TLS communication between nodes.
### Docker Swarm Autolock:
- Provides an un-lock key to un-lock Swarm whenever docker restart.
### Commands:
- Turn on Autolock
```                              
   docker swarm init --autolock=true
   docker swarm update --autolock=true.
```                              
- Turn off Autolock.
```                              
   docker swarm update --autolock=false
```                              
- Unlock Swarm manager
```                              
   docker swarm unlock
```                              
- Retrieve unlock key
```                              
   docker swarm unlock-key
```                              
- Rotate unlock key
```                              
   docker swarm unlock-key --rotate  
```                              

## INTRODUCTION TO DOCKER SERVICES
### Docker Service:
- Allow us to run applications in the Swarm cluster.
- One or more containers can be run across the nodes in Swarm cluster.
### Difference:  
| docker container | run docker service create |
| :--- | :--- |                              
| Runs a single container on a single host | Runs container(s) on 1 to n nodes |
| Not highly available | Highly available |
| Not easily scalable | Easily scalable (up or down) |
| Can’t use -- replicas flag | --replicas used to scale.  |  
                              
### Docker Service CLI:
- Create a service
```                              
    docker service create [image]
```                              
- List Services
```                              
     docker service ls
```                              
- List the task (replica) of a service
```                              
       docker service ps [service name]
```                              
- Delete a service
```                              
        docker service rm [service name]                              
```

##  DOCKER SERVICES
### Scaling a service:
- Scale up or scale down a service that's running across swarm cluster.
- Replica flag used to create replica of containers.
```    
   docker service create --name mynginx --replicas 3 -p 80:80 nginx
```    
### Two ways to scale:
1. docker service update
- docker service update --replicas 5 mynginx
- docker service update --replicas 5 --deatach=true mynginx
  -- detach=true: Not to see progress of service
2. docker service scale
- Scale multiple services at a time.
```    
  docker service scale mynginx=2 mybusybox=3
```   
### Resource Limitation:
Defining containers CPU and memory requirements.
- docker service update --limit-cpu=.5 --reserve-cpu=.25 --limit-memory=124m --reserve-memory=64m mynginx
     Limit
- The maximum value of resource that can be used by container.
     Reservation
- The amount of resource required to run the container
### Template with "docker service create“:
Template is used to give dynamic values.
- Flags can be used:
  --mount
  --hostname
  --env
```    
 docker service create --name mynginx2 --hostname="{{.Node.ID}}-{{.Service.Name}} " nginx
```    

##  REPLICATED AND GLOBAL MODE
### Replicated mode:
- Default mode.
- Can scale the service using --replicas .
```    
 docker service create --name nynginx --replicas 2 -p 80:80 nginx
```    
### Global Mode:
- Can’t scale the service.
- - - replicas flag can’t be used.
```    
  docker service create myglobalnginx -p 8080:80 --mode global nginx
```    
Can’t change the mode of a service
    
## DOCKER SWARM QUORUM
### KEYPOINTS :
- Majority of manager nodes in a swarm.
- More than half of the manager nodes in a swarm.
- Better having odd number of managers in a swarm 
    
### FAULT TOLERANCE
| Managers (N) | Fault Tolerance (N-1)/2 | Quorum/Majority (N/2)+1 |
| :---: | :---: | :---: |    
| 1 | 0 |  1 |
| 2 | 0 |  2 |
| 3 | 1 |  2 |
| 4 | 1 |  3 |
| 5 | 2 |  3 |
| 6 | 2 |  4 |
| 7 | 3 |  4 |
| 8 | 3 |  5 |
    
###  Key points to remember:
- More manager nodes affect the performance of swarm.
- Immediately replace failed manager node.
- Distribute manager nodes across Availability Zone (AZ) for High Availability (HA).
- Take swarm backup.
    
### High Availability:
| Managers | Quorum/Majority | Availability Zones |
| :---: | :---: | :---: |
| 3 | 2 | 1-1-1 |
| 5 | 3 | 2-2-1 |
| 7 | 4 | 3-2-2 |
| 9 | 5 | 3-3-3 |
   Distribution of manager nodes across 3 Availability Zones.
    
## CONSTRAINTS AND LABELS
### Constraint and Label:
Used to control the placement of containers.
### Example 1:
Run tasks only on worker nodes.
 - docker service create --name mynginx_worker \
      --constraint node.role==worker \
      --replicas 3 \
         nginx
### Example 2:
Running tasks on particular node
    1. Label
             -  docker node update --label-add mynode=node1 [Node name]
    2. Constraint
             - docker service create --name mynginx_dc1 \
                 --constraint node.labels.mynode==node1 \
                 --replicas 3 \
                    nginx
### Example 3:
Spread the tasks evenly across all nodes having label as mynode.
            - docker service create --name mynginx_spread \
                 --placement-pref spread=node.label.mynode \
                 --constraint node.role==worker
                 --replicas 4 \
                   nginx   
    
## INTRODUCTION TO DOCKER COMPOSE
### Docker Compose:
Can run multi-container application using different images.
### Install Docker Compose:
- Step 1:
  Download docker compose binary to /usr/local/bin/docker-compose.
```
   sudo curl -L "https://github.com/docker/compose/releases/download/1.26.0/docker
    compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```    
- Step 2:
  Provide executable permission
```    
   sudo chmod +x /usr/local/bin/docker-compose
```    
- Step 3:
  Check the version
```
  docker-compose --version
```
### Docker Compose Commands:
- Create a compose
```
   docker-compose up -d
```   
- List containers created by compose
```    
   docker-compose ps / docker container ls
```    
- Stop a compose
```    
   docker-compose stop
```
- Start a compose
```    
   docker-compose start
```    
- Restart a compose
```
   docker-compose restart
```    
- Delete a compose
```   
  docker-compose down
```
    
##  DOCKER STACK
    Can run services across the swarm.
### Docker Stack Commands:
- Deploy a stack
```    
  docker stack deploy -c [compose file name.yml] [stack name]
```    
- List stacks
```    
  docker stack ls
```
- To see services associated with the stack
```    
  docker stack services [stack name]
```
- To see on what nodes tasks are running
```
  docker stack ps [stack name]
```    
- To see logs of a service
```    
  docker service logs [stack name]
```
- To remove a stack
```
  docker stack rm [stack name]
```

## INTRODUCTION TO DOCKER NETWORKING
### Container Network Model (CNM):
- The Docker networking architecture is built on a set of interfaces called the Container Networking
  Model (CNM).
- libnetwork: is the networking component which implements the CNM.
### Docker network drivers:
1. Bridge
2. Overlay
3. Host
4. None
5. MACVLAN
6. 3rd party network drivers
    
### Building blocks of CNM:
1. Sandbox: Sandbox isolates the networking components of a single
   container such as network interfaces, ports, route tables and DNS.
2. Endpoints: Endpoints are virtual network interfaces and responsibility of
   endpoints is to connect the sandbox to a network.
3. Networks: Network is a collection of endpoints. 
    
## DOCKER NETWORKING COMMANDS
- List Networks
```    
  docker network ls
```
- Create a network
```    
  docker network create [Network Name]
```    
- Inspect a network
```    
  docker network inspect [Network Name]
```    
- Connect a container to a network
```    
  docker network connect [Network Name] [Container Name]
```    
- Disconnect a container from a network
```    
  docker network disconnect [Network Name] [Container Name]
```    
- Create a subnet and gateway
```
  docker network create --subnet 10.1.0.0/24 --gateway 10.1.0.1 [Network Name]
```    
- Assign a specific IP to a container
```    
  docker container run -d --name [Container Name] \
         --ip [IP Address] \
         network [Network Name] \
         nginx
```    
- Remove a network
```    
  docker network rm [Network Name]
```    
- Remove unused networks
```    
  docker network prune
```  
    
## BRIDGE NETWORK 
### Docker Bridge Network:
Default network driver for containers running on a single host. (Not on Swarm).
### Create a bridge network:
```    
docker network create --driver bridge [Network Name]
(OR)
docker network create [Network Name]
```

## EMBEDDED DNS
- Domain Name System (DNS).
- Name of container or services are mapped back to their actual IP address.
- Containers can communicate to each other using container name or service name, or network alias.
### Commands:
```    
  docker network create mynetwork
  docker container run -d --name mynginx --network mynetwork --network-alias mynetworkalias nginx
  docker container run -d --name mybusybox --network mynetwork radial/busyboxplus:curl sleep 1000
  docker exec -it mybusybox /bin/sh
    -  curl mynginx:80
    -  curl mynetworkalias:80
```

## OVERLAY NETWORK
- Overlay network allows containers running on same or
  different nodes (Multiple Hosts) to communicate with each other.
    
- Ingress is the default overlay network.
    
- Use flag --driver=overlay to create custom overlay network.     
### Commands:
- Create a overlay network
```    
  docker network create --driver overlay [Network Name]    
  docker network create --driver overlay --attachable [Network Name]
```    
- Create services with custom network
```    
 docker service create -d --name mynginx --network [Network Name] --replicas 3 -p 80:80 nginx
```
    
## HOST NETWORK 
### Host Network driver:
- No sandbox. No network component isolation.
- Uses Host’s network infrastructure.
- Can not reuse the port.
### Create a Host network:
```
  docker container run -d --name mynginx --network host nginx 
```
    
## NONE NETWORK
- No Networking.
- Container is isolated from other container and also from host.
### Create a none network:
```
  docker container run -d --name mynginxnone --network none -p 8080:80 nginx
```   
    
## PORT PUBLISHING MODES 
### Types of port publishing modes:
1. Ingress
2. Host
#### Ingress:
- The default mode.
- Publishes the port on all hosts i.e. all nodes of a swarm cluster. Routing-mesh.
#####  Create a service using ingress publishing port:
```
 docker service create --name mynginx -p 8080:80 nginx
```    
#### Host:
-  Publishes the port on host where containers are running.
- Runs only one task of a service on the same node.
##### Create a service using host publishing port:
```    
  docker service create --name mynginxhost -p mode=host,published=8081,target=80 nginx 
```
    
## INTRODUCTION TO DOCKER SECURITY
 Uses both the Operating System (OS) and Docker native security features.
### Linux Security Features:
- Namespaces
```    
      Process ID (pid)
      Network (net)
      Filesystem/mount (mnt)
      InterProcess Communication (ipc)
      User (user)
      Unix Timesharing System (uts)
```    
- Cgroups
```    
     CPU
     RAM
```    
- Seccomp
    
### Some of Docker Security Features:
- Docker Content Trust (DCT)
- Docker Security Scanner
- Docker MTLS    
    
### Secure Computing Mode (Seccomp):
- Using Secure Computing Mode (Seccomp) during container creation:
```    
  docker container run --security-opt seccomp=[Profile] Ubuntu
```    
  Example:
```    
      docker container run -it --name myubuntusec --security-opt seccomp=./default.json Ubuntu
```    
### Capabilities:
- Drop a capability:
```    
  docker container run --cap-drop=[Capability] [Image]
```    
 Example:
```    
        docker container run -it --name mybuntucapdrop --cap-drop=MKNOD ubuntu
```    
- Add a capability:
```    
  docker container run --cap-add=[Capability] [Image] 
```    
### Docker Bench for Security:
```    
- docker run -it --net host --pid host --userns host --cap-add audit_control \
   -e DOCKER_CONTENT_TRUST=$DOCKER_CONTENT_TRUST \
   -v /etc:/etc:ro \
   -v /usr/bin/containerd:/usr/bin/containerd:ro \
   -v /usr/bin/runc:/usr/bin/runc:ro \
   -v /usr/lib/systemd:/usr/lib/systemd:ro \
   -v /var/lib:/var/lib:ro \
   -v /var/run/docker.sock:/var/run/docker.sock:ro \
   --label docker_bench_security \
  docker/docker-bench-security
```
    
## DOCKER CONTENT TRUST (DCT)
- Verify integrity and publisher of an Image.
- Pull and run signed images.
    
### Steps to set-up DCT:
Step 1: Log into the Docker Hub
```   
 docker login
```    
Step 2: Generate a key (.pub)
```    
 docker trust key generate [Docker hub username]
```    
Step 3: Add signer to an image repository:
```    
 docker trust signer add --key [.pub] [Docker hub username] [repository] 
```  
Step 4: Enable Docker Content Trust (DCT)
```    
  export DOCKER_CONTENT_TRUST=1
```    
Step 5: Sign and push image to registry
```    
  docker trust sign [Image]:[Tag]
```
    
### Disable Docker Content Trust (DCT):
```    
 export DOCKER_CONTENT_TRUST=0
```    
    
### Logout of Docker hub:
```
 docker logout 
```
    
## DOCKER MTLS AND ENCRYPTED OVERLAY NETWORK
### Mutually Authenticated Transport Layer Security (MTLS):
- Docker Swarm uses mutual Transport Layer Security (TLS) for communication and authentication
  between nodes.
### To Create an encrypted overlay network:
```    
  docker network create --opt encrypted --driver overlay [Network Name
```
    
## UNINSTALL DOCKER ENGINE    
- sudo systemctl stop docker
- sudo apt-get remove -y docker-ce docker-ce-cli
- sudo apt-get update
    
## LOGGING DRIVERS
By default Docker uses json-file logging driver. 
    
### SUPPORTED LOGGING DRIVERS:    
    
### Check default Logging driver:
- docker info
- docker info | grep storage
    
#### Method -1 : Edit unit file (docker.service)
- Add --storage-driver flag
```
  sudo vi /usr/lib/systemd/system/docker.service
  ExecStart=/usr/bin/dockerd --storage-driver devicemapper
```    
- Restart the docker
```    
  sudo systemctl daemon-reload
  sudo systemctl restart docker
```    
    
#### Method 2: Configuration file (daemon.json)
- Configure daemon file
```    
  sudo vi /etc/docker/daemon.json
    {
        "log-driver":"syslog"
    {
```    
- Restart Docker
```    
  sudo systemctl restart docker
  sudo systemctl status docker 
```    
