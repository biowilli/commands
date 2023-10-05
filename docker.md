# Docker Commands

This document lists some common Docker commands that are used to manage Docker containers and images.

## Managing Containers

| Command                          | Description                                                             |
| -------------------------------- | ----------------------------------------------------------------------- |
| `docker pull image_name`         | Pulls a Docker image from a registry.                                   |
| `docker run -it image_name`      | Runs a Docker container from an image in interactive mode.              |
| `docker run -d image_name`       | Runs a Docker container in detached mode.                               |
| `docker ps`                      | Lists all running containers.                                           |
| `docker ps -a`                   | Lists all containers, including stopped ones.                           |
| `docker stop container_id`       | Stops a running container.                                              |
| `docker start container_id`      | Starts a stopped container.                                             |
| `docker restart container_id`    | Restarts a running container.                                           |
| `docker rm container_id`         | Removes a container.                                                    |


## Copy files inside Containers

| Command                          | Description                                                             |
| -------------------------------- | ----------------------------------------------------------------------- |
| `docker cp /path/to/local/file container_id:/path/in/container/destination`         | You can copy a file from your local system into a running Docker container using the docker cp command.                                   |

## Managing Images

| Command                        | Description                                                           |
| ------------------------------ | --------------------------------------------------------------------- |
| `docker images`                | Lists all Docker images on your system.                              |
| `docker rmi image_id`          | Removes a Docker image.                                              |
| `docker pull image_name:tag`   | Pulls a specific version (tag) of a Docker image from a registry.   |
| `docker build -t image_name .` | Builds a Docker image from a Dockerfile in the current directory.   |

## Networking

| Command                                 | Description                                              |
| --------------------------------------- | -------------------------------------------------------- |
| `docker network ls`                     | Lists all Docker networks on your system.               |
| `docker network create network_name`    | Creates a new Docker network.                           |
| `docker network connect network_name container_id` | Connects a container to a network.         |

## Miscellaneous

| Command               | Description                                       |
| ---------------------  | ------------------------------------------------- |
| `docker exec -it container_id bash` | Opens a Bash shell inside a running container. |
| `docker logs container_id` | Displays the logs of a container.         |
| `docker-compose up`    | Starts services defined in a `docker-compose.yml` file. |
| `docker-compose down`  | Stops and removes services started with `docker-compose up`. |

Source: [Docker Documentation](https://docs.docker.com/)
