# aspnetcore-microservices
Test 4
+
development 2
main 2
main 3

## Helper commands

### Docker terminal commands

##### check docker run:
docker ps

##### check docker stoped containers
docker ps -a

##### load docker image from https://hub.docker.com/_/mongo?tab=description
docker pull mongo
 
##### run docker container:
docker run -d -p 27017:27017 --name shopping-mongo mongo 

*	d - means detach
*	p - means port forwarding
*	shopping-mongo - container name
*	mongo - container image

##### execute command in existing docker container
docker exec -it shopping-mongo /bin/bash

*	it - interactive terminal
*	shopping-mongo - container name
*	/bin/bash - path

##### execute mongo application
mongo
show dbs
show collections

##### start docker container
docker start mongo

##### stop all containers
docker stop $(docker ps -aq)

##### remove all containers
docker rm $(docker ps -aq)

##### remove all images
docker rmi $(docker images -q)

##### remove everything and clenup
docker system prune

#### docker compose
Use to load and build images and run containers

##### start
docker-compose  -f docker-compose.yml -f docker-compose.override.yml up -d

##### stop
docker-compose  -f docker-compose.yml -f docker-compose.override.yml down

### ASP.NEt Web API

https://docs.microsoft.com/en-us/aspnet/core/web-api/action-return-types?view=aspnetcore-6.0

### NuGet
https://www.nuget.org/packages/

### Redis
docker pull redis
docker exec -it aspnetrun-redis /bin/bash

##### Run Redis CLI:
redis-cli

##### Redis CLI commands
ping
set key value
get key
