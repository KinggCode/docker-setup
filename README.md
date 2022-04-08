# Docker Setup 
Installation Set up for Linux Distros : Ubuntu, Debian, CentOs

#Upgrade apt-get package 
```sh
sudo apt-get update && sudo apt-get upgrade
```

#Install docker packages 
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

#Install Docker Engine for Ubuntu 
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
