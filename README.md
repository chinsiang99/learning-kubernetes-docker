# multi-container pods
- most common scenario: Helper process

![multi-container-pods](multi-container-pods.png)

## Typical patterns - sidecar
![sidecar](sidecar.png)

## typical patterns - adapter
![adapter](adapter.png)

## typical patterns - ambassador
![ambassador](ambassador.png)

## Multi container yaml file
![yaml-file](yaml-file.png)

## Cheatsheet
![cheat-sheet](cheat-sheet.png)

# Networking Concepts
- All containers within a pod can communicate with each other
- All pods can communicate with each other
- All nodes can communicate with all pods
- Pods are given an IP address (ephemeral)
- Services are given a persistent IP

## Pod networking
![pod-networking](pod-networking.png)

## inter pod communication
![inter-pod](inter-pod.png)

## External access
![external-access](external-access.png)