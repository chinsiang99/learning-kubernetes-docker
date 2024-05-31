# Container registries

## What are Container Registries?
- Central repositories for container images
- Private or public
- Docker Hub
    - hub.docker.com
- Microsoft
    - Azure Container Registry
    - Microsfot Container Registry (public images)
- Amazon Elastic Container Registry
- Google Container Registry

## Publish to Docker Hub

1. login to Docker Hub
> docker login -u <username> -p <password>

2. tag the image previously built
> docker tag my_image chinsiang99/my_image:latest

3. push the image
> docker push chinsiang99/my_image:latest

4. pull the image
> docker pull chinsiang99/my_image:latest