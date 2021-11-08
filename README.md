# docker_project0
Project for nodejs development with Docker

Steps for app development with Docker:

1. Install docker on the hosting machine.
2. Pull the needed docker images from private/public docker hub - ```docker pull image_name:version```
3. Create network for the docker containers to be able to communicate with them - ```docker network create network_name```
4. Run the containers using their images: ```docker run -d -p port:port -e ADDITIONAL_VAR=var_value -e ADDITIONAL_VAR2=var2_value --net network_name --name container_name image_name:version```
5. Create app locally with help of containerized apps that you've installed.


Docker Compose:

In order to do stuff more efficient - we will use docker-compose file, which will allow us to compose some containers running method in the same file.
