## Generic commands
- **`docker run`**: This command is used to create a container from an image and start it. For example, `docker run ubuntu` will start a container with the Ubuntu image.
- **`docker ps`**: This command lists all the running containers. You can use the `-a` or `--all` flag to show all containers (both running and stopped).
- **`docker stop`**: This command stops a running container. For example, `docker stop my_container` will stop the container named "my_container".
- **`docker rm`**: This command removes one or more containers. For example, `docker rm my_container` will remove the container named "my_container".
- **`docker images`**: This command lists all the Docker images on your system.
- **`docker rmi`**: This command removes one or more images. For example, `docker rmi ubuntu` will remove the Ubuntu image.
- **`docker pull`**: This command pulls an image from a Docker registry. For example, `docker pull ubuntu` will pull the latest Ubuntu image from Docker Hub.
- **`docker exec`**: This command allows you to run a command in a running container. For example, `docker exec my_container ls` will run the `ls` command in the "my_container" container.
- **`docker build`**: This command is used to build an image from a Dockerfile. For example, `docker build -t my_image .` will build an image named "my_image" using the Dockerfile in the current directory.
- **`docker login`** and **`docker logout`**: These commands are used to log in to and log out from a Docker registry.
- **`docker version`**: This command shows the version of Docker that is currently installed.
- **`docker info`**: This command displays system-wide information about Docker.


## Create and run containers
###Kali   
`docker pull docker.io/kalilinux/kali-rolling`   
`docker run --tty --interactive kalilinux/kali-rolling`   
   
###Ubuntu   
`docker pull ubuntu`   
or for specific version   
`docker pull ubuntu:24.04`   
`docker run -ti --rm ubuntu /bin/bash`   
