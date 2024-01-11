# Docker Command Cheat Sheet

## Docker Lifecycle Commands
| Command | Use |
| :--- | :--- |
| docker create | Create a new container |
| docker run | Creates a docker container from docker image |
| docker pause | To pause a running container |
| docker unpause | To unpause a running container |
| docker stop | To stop a docker container |
| docker start | To start a docker container |
| docker restart | To restart docker container |
| docker attach | Attach Terminal to Running container |
| docker wait | Block until one or more containers stop, then print their exit codes |
| docker rm | To remove the Docker Container, stop it first and then remove it |
| docker kill | To stop and remove Docker containers |

## Docker Basic Commands
| Command | Use |
| :--- | :--- |
| docker | To check all available Docker Commands
| docker version | To show Docker version |
| docker info | Displays system wide information |
| docker pull | To pull the docker Images from Docker Hub Repository |
| docker build | To Docker Image from Dockerfile |
| docker run | Run a container from a docker|
| docker commit | To commit a changes in container file OR create new Docker Image |
| docker ps  | List all the running containers. Add the -a flag to list all the containers. |
| docker start | To start a docker container |
| docker stop | To stop a docker container |
| docker logs | To view Logs for a Docker Container |
| docker rename | To rename Docker Container |
| docker rm | To remove the Docker Container, stop it first |

## Docker Image Commands
| Command | Use |
| :--- | :--- |
| docker build | To build Docker Image from Dockerfile |
| docker pull | To pull Docker Image from Docker Hub Registry |  
| docker tag | To add Tag to Docker Image |
| docker images | To list Docker Images |
| docker push | To push Docker Images to |
| docker history | To show history of Docker Image |
| docker inspect | To show complete information in JSON format |
| docker save | To save an existing Docker Image |
| docker import | Create Docker Image from Tarball |
| docker load | To export existing Docker |
| docker rmi | To remove docker images |
| docker export | To load Docker Image from file or archives |

## Docker Container Commands
| Command | Use |
| :--- | :--- |
| docker start | To start a Docker container |
| docker stop | To stop a running docker container |
| docker restart | To restart docker container |
| docker pause | To pause a running container |
| docker unpause | To unpause a running container |
| docker run | Creates a docker container from docker image |
| docker ps | To list Docker containers |
| docker exec | To Access the shell of Docker Container |
| docker logs | To view Logs for a Docker Container |
| docker rename | To rename Docker Container |
| docker rm | To remove Docker container |
| docker stop | To stop a running docker container |
| docker attach | Attach Terminal to Running container |
| docker kill | To stop and remove Docker containers |
| docker inspect | Docker container info command |
| docker cp | To copy files or folders between a container and from local filesystem. |

## Docker Compose Commands
| Command | Use |
| :--- | :--- |
| docker-compose build | To build docker compose file |
| docker-compose up | To run docker compose file |
| docker-compose ls | To list docker images declared inside docker compose file |
| docker-compose start |  To start containers which are already created using docker compose file |
| docker compose run | To run one one of application inside docker5. docker-compose run compose.yml |
|  docker-compose rm | To remove docker containers from docker compose |
|  docker-compose ps | To check docker container status from docker compose |

## Docker Volume Commands
| Command | Use |
| :--- | :--- |
| docker volume create | To create docker volume |
| docker volume inspect | To inspect docker volume |
| docker volume rm | To remove docker volume |

## Docker Networking Commands
| Command | Use |
| :--- | :--- |
| docker network create | To create docker network |
| docker network ls | To list docker networks |
| docker network inspect | To view network configuration details |

## Docker Logs and Monitoring Commands
| Command | Use |
| :--- | :--- |
| docker ps -a | To show running and stopped containers |
| docker logs | To show Docker container logs |
| docker events | To get all events of docker container |
| docker top | To show running process in docker container |
| docker stats usage | To check cpu, memory and network I/O |
| docker port | To show docker containers public ports |

## Docker Prune Commands
| Command | Use |
| :--- | :--- |
| docker system prune |  To clean all resources which are dangling or not associated with any docker containers |
| docker image prune | To remove Dangling Docker images |
| docker container prune | To remove all unused docker containers |
| docker volume prune | To remove all unused docker volumes |
| docker network prune | To remove all unused docker network |

## Docker Hub Commands
| Command | Use |
| :--- | :--- |
| docker search | To search docker image |
| docker pull | To pull image from docker hub |
| docker login | To Log in to a Docker registry |
| docker push | Push an image or a repository to a registry |
| docker tag | Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE |
| docker logout | To logout from Docker Hub Registry |
 
