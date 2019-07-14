# Docker commands

docker ps : list running containers
docker stop [CONTAINER_ID] : stop the running container
docker logs -f [CONTAINER_ID] : display contauiner logs
docker run -p 27017:27017 -d mongo  : launch container for mongo
docker images : list local images
docker exec -it <container name> bash : shell into a container
docker kill $(docker ps -q) : kill all containers
docker rm $(docker ps -a -q) : delete all stopped containers
docker rmi <image name> : remove docker image
docker rmi ${docker images -q -f dangling=true} : delete untagged images
docker rmi ${docker images -q} : delete all images
docker volume rm ${docker volume ls -f dangling=true -q} : remove all dangling volumes


docker run -d --hostname ancm-rabbit --name some-rabbit -p 8080:15672 -p 5671:5671 -p 5672:5672 rabbitmq:3.8-rc-management : start rabbitmq
docker run --name ancm-mysql -e MYSQL_ALLOW_EMPTY_PASSWORD=yes -v C:/Users/chamo/programmation/formations/dockerdata/mysql:/var/lib/mysql -p 3306:3306 -d mysql


# Resources

- https://springframework.guru/docker-cheat-sheet-for-spring-devlopers/