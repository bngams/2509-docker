# CLuster

Intro: https://docs.docker.com/engine/swarm/stack-deploy/

docker run -d --privileged --name worker-1 --hostname=worker-1 -p 12375:2375 docker:latest

docker exec worker-1 docker swarm join --token "$(docker swarm join-token -q worker)" "$(docker info --format '{{.Swarm.NodeAddr}}'):2377"