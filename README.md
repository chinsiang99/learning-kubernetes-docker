# Docker CLI Cheat Sheet 

## Docker CLI Cheat Sheet - Management

| Command    | Description                         |
|------------|-------------------------------------|
| docker info  | Display system information  |
| docker version  | Display the system's version  |
| docker login  | Login to a Docker registry  |

## Docker CLI Cheat Sheet - Running and stopping
| Command    | Description                         |
|------------|-------------------------------------|
| docker pull [imageName]  | Pull an image from a registry  |
| docker run [imageName]  | Run containers  |
| docker run -d [imageName]  | Run in detached mode  |
| docker start [containerName]  | Start stopped containers  |
| docker ps  | List running containers  |
| docker ps -a  | List running and stopped containers  |
| docker stop [containerName]  | Stop containers  |
| docker kill [containerName]  | Kill containers  |
| docker image inspect [imageName]  | Get image info  |

## Docker CLI Cheat Sheet - Limits
| Command    | Description                         |
|------------|-------------------------------------|
| docker run --memory="256m" nginx  | Max memory  |
| docker run --cpus=".5" nginx  | Max CPU  |

## Docker CLI Cheat Sheet - Attach Shell
| Command    | Description                         |
|------------|-------------------------------------|
| docker run -it nginx -- /bin/bash | Attach Shell  |
| docker run -it -- microsoft/powershell:nanoserver  | Attach Powershell |
| docker container exec -it [containername] -- bash  | Attach to a running container |

## Docker CLI Cheat Sheet - Cleaning up
| Command    | Description                         |
|------------|-------------------------------------|
| docker rm [containerName]  | Removes stopped containers  |
| docker rm $(docker ps -a -q)  | Removes all stopped containers  |
| docker images  | List images |
| docker rmi [imageName] | Deletes the image |
| docker system prune -a | Removes all images not in use by any containers |

## Docker CLI Cheat Sheet - Building
| Command    | Description                         |
|------------|-------------------------------------|
| docker build -t [name:tag] .  | Builds an image using a Dockerfile located in the same folder |
| docker build -t [name:tag] -f [fileName]  | Builds an image using a Dockerfile located in a different folder  |
| docker tag [imageName] [name:tag]  | Tag an existing image |

## Dockerfile - Node site
FROM alpine # base image
RUN apk add -update nodejs nodejs-npm # Install Node and NPM using the package manager
COPY . /src
WORKDIR /src
RUN npm install
EXPOSE 8080 # tells the container to listen on port 8080
ENTRYPOINT ["node", "./app.js"] # What to run
