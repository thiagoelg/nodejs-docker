# nodejs-docker
Docker image for node-js, runing with the traefik service

# Prerequisites
You will need both **Docker**, **docker-compose** and **Nodejs with NPM**.

### - Installing Docker
https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-16-04

### - Installing docker-compose
https://www.digitalocean.com/community/tutorials/how-to-install-docker-compose-on-ubuntu-16-04

### - Installing lates nodejs + npm
https://github.com/creationix/nvm#install-script

# Preparing your environment

We need to edit our hosts file so our machine recognize the traefik domains we will be using.
As ou can see in the docker-compose.yml, traefik is using ```localhost.node``` and ```localhost.phpmyadmin```.

Edit your hosts file with the following command:
> ```sudo nano /etc/hosts```

Then, add these lines:
> 127.0.0.1 localhost.node

> 127.0.0.1 localhost.phpmyadmin

Save and exit.

# Running your server

- Install node dependencies:
> ```cd app && npm install && cd ..```

- Create the docker network used by the containers:
> ```docker network create node```

- Then run your server with:
> ```sudo docker-compose up```

- Or run it in the background with:
> ```sudo docker-compose up -d```
