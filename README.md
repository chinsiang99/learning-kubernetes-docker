# Deployments
- A deployment manage a single pod template
- You create a deployment for each microservice
    - front-end
    - back-end
    - image-processor
    - creditcard-processor
- create ReplicaSets in the background
- dont interact with replicaSets directly

![deployments](deployments.png)

## Deployments definition in yaml file
- replicas
    - number of pod instances
- revisionHistoryLimit
    - number of previous iterations to keep
- strategy
    - rollingUpdate
        - cycle through updating pods
    - recreate
        - all existing pods are killed before new ones are created

![deployment-definition](deployment-definition.png)

![final-deployment-definition](final-deployment-definition.png)

## kubectl cheatsheet
![deployment-cheatsheet](deployment-cheatsheet.png)