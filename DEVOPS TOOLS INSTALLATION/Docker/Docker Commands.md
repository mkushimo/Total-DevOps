# Docker Commands

- docker info: It will give status of weather docker is running or not  and also It will display the detailed information about docker engine. 

- docker version: Show the Docker version information.

- docker images (OR) docker image ls : List all images that are locally stored with the Docker engine.

- docker run <<Docker Image>> : It will run the docker image.

  Example: docker run hello-world: This command will download the hello-world image, if it is not already present, and run the hello-world as a container.

- docker images <<Image Name>>: It will display the information about image.

- docker images -q: It will display only the images IDs.

- docker rmi << Image ID/Image Name>> (OR) docker image rm << Image ID/Image Name>>: It will delete an image from the local image store.
  Example: docker rmi nginx

- docker rmi $(docker images -q) (OR) docker rmi -f $(docker images -q) : It will remove all the images from docker engine.

- docker run --name “hello-world-container” helloworld: Start the hello-world image with “hello- world-container” container name. 

- docker create “hello-world-cont” helloworld : It will create a container called “hello-world-cont” from the image hello-world and it won’t start the container.

- docker ps (OR) docker container ls: Lists running containers (It will not display the stopped containers)

- docker ps –a (OR) docker container ls --all (OR) docker container -a: Lists all containers (It will display the stopped containers along with running containers.)
                                                    
- docker start <Container name|id>: It will start the container.

- docker start webserver: It will start the webserver.

- docker stop <container name|id> (OR) docker container stop <container name|id>: It will stop the docker container.

- docker stop webserver: It will stop the container called webserver.

- docker pause CID/CNAME: It will pause the container.

- docker unpause CID/CNAME: It will unpause the container.

## Docker Container status are, created, restarting, running, removing, paused, exited, or dead

- docker ps -a --filter "name=mithun16thjune": It will display all the containers with name mithun16thjune name.

- docker ps -a --filter 'exited=0' :

- docker ps --filter status=running: It will display the all the running state containers.

- docker ps --filter status=paused: It will display the all the paused state containers.

- docker logs <container name>: It will display the logs for that container.

- docker logs --tail 100 <<Container Name>>: Print the last 100 lines of a container’s logs.

- docker top <<Container ID>>: This will shows the top processes in within in a container.

- docker reanme <<Container Old Name>> <<Container New Name>>: It will rename the conatiner.

- docker rm -f <<Container Name>>: It will remove the container.

- docker rm -f webserver: It will stop and remove the running container with a single command.

- docker stop $(docker ps -a -q): It will stop all the containers.

- docker rm -f $(docker ps -aq): Delete all running and stopped containers.

- docker kill <<CID/C Name>>: It will kill the container.

-  container prune: It will delete all stopped containers.

- docker search <<Image Name>>: It will search all of the publicly available images on Docker Hub(https://hub.docker.com).

- docker pull <<Image Name>: Pull an image from Docker Hub

- docker inspect <<CID>> : It will give information for container.

- docker attach <<CID>> : It will connect to running container.

- docker exec <<CID>> : Run a linux command in a running container.

- docker stats <<CID>> : It will display a live stream of container resource usage statics.

- docker network ls: List the networks.

- docker network create mithuntechnologies : It will create the network with name called as mithuntechnologies.

- docker network inspect bridge: Display detailed information on one or more networks.

- docker network connect: Connect a container to a network.

- docker network prune: Remove all unused networks.

- docker run -it -v /Users/mithunreddyl/Desktop/dockervolumes:/mithuntechnoVol1 ubuntu : Create a container with volume mithuntechnoVol1.

- docker run -it -v /Users/mithunreddyl/Desktop/dockervolumes:/mithuntechnoVol1:ro --name ubuntucontainer16 ubuntu : Create the Read only Volume.

- docker run -it --volumes-from ubuntucontainer16 --name ubuntucontainer1604 ubuntu:16.04: Create a container ubuntucontainer1604 that uses the same volumes as ubuntucontainer16

Can I mount same volume to multiple docker containers?
```
Ans) Yes you can add same location as a volume to many docker containers.
```
  
- docker login: To sign into the Docker Hub.

- docker logout: To logout from the Docker Hub. If no server is specified, then the default is used.
