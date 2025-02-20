# Cheat sheets and checklists

- Student name: Hanno van Baarle
- GitHub repo: URL

## Basic commands

| Task              | Command           |
| :---------------- | :---------------- |
| Change directory  | `cd DIRECTORY`    |
| List files        | `ls -l`           |
| Create directory  | `mkdir DIRECTORY` |
| Create empty file | `touch FILE`      |
| Copy file         | `cp FILE DEST`    |
| Move file         | `mv FILE DEST`    |

## Docker commands

| Task                                        | Command                                                           |
| :------------------------------------------ | :---------------------------------------------------------------- |
| List all containers                         | `docker ps -a`                                                    |
| List all images                             | `docker images`                                                   |
| Stop a container                            | `docker stop CONTAINER`                                           |
| Remove a container                          | `docker rm CONTAINER`                                             |
| Remove an image                             | `docker rmi IMAGE`                                                |
| pull image from dockerhub                   | `docker build --platform linux/amd64 -t hannodocker/dockerlab1 .` |
| push image to dockerhub                     | `docker push hannodocker/dockerlab1`                              |
| use docker compose file to start containers | `docker compose up -d`                                            |
| stop containers                             | `docker compose down`                                             |
| build container                             | `docker build -t webapp .`                                        |

## Kubernetes commands

| Task                                           | Command                                      |
| :--------------------------------------------- | :------------------------------------------- |
| Start minikube with docker                     | `minikube start --driver=docker`             |
| interact with cluster                          | `minikube kubectl -- get po -A`              |
| real-time view on what happens on your cluster | `kubectl get all`                            |
| get which node is running which pod            | `kubectl get pods --all-namespaces -o wide`  |
| check logs of pod                              | `kubectl logs -f <name>`                     |
| Delete pods with certain label                 | `kubectl delete pods --selector <statement>` |
| More commands in the lab report                | `other commands in the lab report`           |

## Git workflow

Simple workflow for a personal project without other contributors:

| Task                                         | Command                   |
| :------------------------------------------- | :------------------------ |
| Current project status                       | `git status`              |
| Select files to be committed                 | `git add FILE...`         |
| Commit changes to local repository           | `git commit -m 'MESSAGE'` |
| Push local changes to remote repository      | `git push`                |
| Pull changes from remote repository to local | `git pull`                |
| initialize github repo                       | `git init`                |

## Checklist network configuration

1. Is the IP address correct? `ip a`
2. Is the router/default gateway correct? `ip r -n`
3. Is a DNS-server available? `cat /etc/resolv.conf`
