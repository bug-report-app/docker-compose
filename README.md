# Docker Compose - Bug Report App

## Prerequisites

- Docker Engine 19.03.0+

  - **Linux:** Follow all the steps present in the [official documentation](https://docs.docker.com/install/linux/docker-ce/ubuntu/#install-docker-ce)

- Docker Compose 1.26.0+
  - Follow all the steps present in the [official documentation](https://docs.docker.com/compose/install/)

## Getting Started

1. **Clone this repository and submodules**

   ` git clone --recurse-submodules git@github.com:bug-report-app/docker-compose.git`

## Building and Deploying the containers

```sh
docker-compose up --build -d
```

## Stopping the execution

To stop all containers created by docker-compose, you need to go to the folder where docker-compose.yml is and run:

```sh
docker-compose down
```

---

## Other useful commands

Restarts Docker. Useful in critical situations:

```sh
sudo service docker restart
```

Check all containers and its status:

```sh
docker container ls
```

Enter in the shell or bash of a particular container:

```sh
docker exec -it container_id /bin/bash
```

Stop all containers:

```sh
docker stop $(docker ps -a -q)
```

Delete all containers:

```sh
docker rm -f $(docker ps -a -q)
```

Delete all volumes:

```sh
docker volume rm $(docker volume ls -q)
```

Delete all container images:

```sh
docker rmi -f $(sudo docker images -q)
```

Update modules:

```sh
git submodule update --init --recursive
```

and

```sh
git submodule update --recursive --remote
```
