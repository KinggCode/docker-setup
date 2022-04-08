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

Check if the docker engine is installed successfully
```sh
docker -v 
```


# Git Best Practices for Team Collaboration
When you're the only member working a project and pushing code to any repo, Git can be very basic. Everything is just add, commit, push, and repeat the cycle.

### Clone the project
```sh
git clone <repo-name>
```

### Open the repo: cd REPONAME 
```
cd ElectronicShop
```

### Ensure you are on the main branch
```
git checkout main
```

### Ensure you are up-to-date with the main

Pull in any new code from the main branch: `git pull origin main`

Resolve any merge conflicts that may now be revealed

```
git pull origin main
```

### Create a new branch for your task
```sh
git checkout -b BRANCHNAME
```

### Open VS Code: 

```
code .
```

### Make all your edits
Add all your updates

```
git add .
```

### Commit your updates
```
git commit -m "[FILENAME] UPDATE"
```
`Example`
```
git commit -m "[README] Updated"
```

### Push to the branch

```
git push origin BRANCHNAME
```

## Make a pull request to merge with main branch
When you are done and your code is very clean, request a PR via the GitHub page to merge with the master branch. Request for a review for it to be merged


# Frontend Folder Structure Best Practices 


# Backend Folder Structure Best Practices 


# Cloud Hosting  Best Practices 

#Web Platform Security  Best Practices 
