# docker_project0
Project for nodejs development with Docker

Steps for app development with Docker:

1. Install docker on the hosting machine.
2. Pull the needed docker images from private/public docker hub - ```docker pull image_name:version```
3. Create network for the docker containers to be able to communicate with them - ```docker network create network_name```
4. Run the containers using their images: ```docker run -d -p port:port -e ADDITIONAL_VAR=var_value -e ADDITIONAL_VAR2=var2_value --net network_name --name container_name image_name:version```
  for example of the mongodb and mongo express:
  ```docker run -d -p 27017:27017 -e MONGO_INITDB_ROOT_USERNAME=admin -e MONGO_INITDB_ROOT_PASSWORD=password --name mongodb --net mongo-network mongo:4.4.1```
  ```docker run -d -p 8081:8081 -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin -e ME_CONFIG_MONGODB_ADMINPASSWORD=password --net mongo-network --name mongo-express -e ME_CONFIG_MONGODB_SERVER=mongodb mongo-express```
6. Create app locally with help of containerized apps that you've installed.


Docker Compose:

In order to do stuff more efficient - we will use docker-compose file, which will allow us to compose some containers running method in the same file.
It also takes care of a network for the containers so we don't need to add one manually.
