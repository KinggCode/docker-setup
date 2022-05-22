# Docker Setup 
Installation Set up for Linux Distros : Ubuntu, Debian, CentOs

# Upgrade apt-get package 
```sh
sudo apt-get update && sudo apt-get upgrade
```

# Install docker packages 
```sh
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
```
# Add Docker’s official GPG key:
```sh
 curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

```
Use the following command to set up the stable repository. To add the nightly or test repository, add the word nightly or test (or both) after the word stable in the commands below. Learn about nightly and test channels.

```sh
 echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

```

# Install Docker Engine for Ubuntu 
```sh
sudo apt-get install -y docker.io
```

Check if the docker engine is installed successfully and version installed
```sh
docker -v 
```

Run Hello world app to check if docker engine is up and running
```sh
sudo docker run hello-world
```
This command downloads a test image and runs it in a container. When the container runs, it prints a message and exits.

# Uninstall Docker Engine for Ubuntu 
```sh
sudo apt-get install -y docker.io
```

#Remove all containers, images and volumes from directory 

```sh
sudo rm -rf /var/lib/docker
sudo rm -rf /var/lib/containerd
```

# DockerFile

Run this to build Dockerfile 
```sh 
docker build -t node-app:1.0 .
```

# Display Docker Images 
```sh
sudo docker images 
```

# Docker Commands 

Download docker images from Docker Hub Registry 
```sh 
docker run <ImageName>
```

Display all docker images within the system 
```sh 
docker images
```

Display all docker images ID within the system 
```sh 
docker images -q
```

Show more details about an image  
```sh 
docker inspect <ImageName>
```

To delete a docker image
```sh 
docker rmi <ImageID>
```


List all running containers within the system
```sh 
docker ps
```

List all containers within the system
```sh 
docker ps -a 
```

Get all commands run against the docker image 
```sh 
docker history <ImageID>

OR

docker history <ImageName>

```

# Docker Container Commands

View top processes within the container
```sh 
docker top <ContainerId>
```

Stop docker container from running 
```sh 
docker stop <ContainerId>
```

Delete docker container
```sh 
docker rm <ContainerId>
```



