# nodejs-docker
Docker image for node-js, runing with the traefik service

# Running your server

- Install node dependencies:
> ```cd app && npm install```

- Create the docker network used by the containers:
> ```docker network create node```

- Then run your server with:
> ```sudo docker-compose up```

- Or run it in the background with:
> ```sudo docker-compose up -d```
