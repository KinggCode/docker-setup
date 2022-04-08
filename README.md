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



# Getting Started as an Viewer 
First, create a folder in our enevironment 
```sh
mdkir <New Directory> 
```

# Getting Started as an Viewer 
First, create a folder in our enevironment 
```sh
mdkir <New Directory> 
```

Change Directory into new folder created 
```sh
cd <New Directory> 
```

Clone the git repository 
```sh
git clone git@github.com:KinggCode/ElectronicShop.git
```

Open the Git folder in any text editor of your choice 
Some available free editor can be found at Atom.io, Visual Studio, Notepad ++, Bracelets and many others 

Make a duplicate copy of the env.example and name the new file .env
```sh
touch .env
```
Make sure you are the root diretcory of the Git folder before executing the command above 


Now, it is time to copy all the content from the .env.example into our newly created file (.env)
```sh
cat .env.example > .env 
```

The .env contains the below content after copying 
```sh
APP_NAME=Laravel
APP_ENV=local
APP_KEY=
APP_DEBUG=true
APP_URL=http://localhost

LOG_CHANNEL=stack
LOG_DEPRECATIONS_CHANNEL=null
LOG_LEVEL=debug

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=

BROADCAST_DRIVER=log
CACHE_DRIVER=file
FILESYSTEM_DISK=local
QUEUE_CONNECTION=sync
SESSION_DRIVER=database
SESSION_LIFETIME=120

MEMCACHED_HOST=127.0.0.1

REDIS_HOST=127.0.0.1
REDIS_PASSWORD=null
REDIS_PORT=6379

MAIL_MAILER=smtp
MAIL_HOST=mailhog
MAIL_PORT=1025
MAIL_USERNAME=null
MAIL_PASSWORD=null
MAIL_ENCRYPTION=null
MAIL_FROM_ADDRESS="hello@example.com"
MAIL_FROM_NAME="${APP_NAME}"

AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_DEFAULT_REGION=us-east-1
AWS_BUCKET=
AWS_USE_PATH_STYLE_ENDPOINT=false

PUSHER_APP_ID=
PUSHER_APP_KEY=
PUSHER_APP_SECRET=
PUSHER_APP_CLUSTER=mt1

MIX_PUSHER_APP_KEY="${PUSHER_APP_KEY}"
MIX_PUSHER_APP_CLUSTER="${PUSHER_APP_CLUSTER}"

GCP_PROJECT_ID=
GCP_REGION_ID=
GCP_ZONE_ID=
GCP_SERVICE_ACCOUNT=
GCS_BUCKET=electronic/

```

Now its time to upate the database credentials to match the hosted DB or local server 
```sh

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=

```
Update Composer Package to enable artisan and other composer package
Failure to do so would result in an error 
```sh
composer update 
```

Update Composer Package to enable artisan and other composer package
Failure to do so would result in an error 
```sh
php artisan migrate:fresh
```


Upload some dummy entries into the dashboard 
```sh
php artisan db:seed
```

Run the PHP Engine
```sh
php artisan serve 
```


# Understanding Electronic Shop Directory 

```sh
Front 
  |___ Cart
    |___ index.blade.php
  |___ Catalogue
    |___ index.blade.php
  |___ Checkout
    |___ index.blade.php
  |___ Components
    |___ navbars
        |___ default.blade.php
    |___ styles
        |___ default.blade.php
    |___ scripts
        |___ default.blade.php
    |___ footers
        |___ default.blade.php
    |___ breadcrumbs
        |___ default.blade.php
    |___ information_bars
        |___ default.blade.php
    |___ product_modals
        |___ default.blade.php
  |___ Contact
    |___ index.blade.php
  |___ General
    |___ home.blade.php
  |___ Orders
    |___ index.blade.php
  |___ Shop
    |___ index.blade.php
  |___ Wishlist
    |___ index.blade.php
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
