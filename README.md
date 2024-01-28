# DevOps-Assignment-2 Part 1
DevOps-Assignment-2 Part 1

 - Create a new Docker network named "my_network" using the bridge driver
    - docker network create --driver=bridge my_network
 - Create a new Docker container using the "nginx" image and connect it to the "my_network" network. Name the container "nginx_container".
    - docker pull nginx
    - docker run --name nginx_container --network my_network -d nginx
 - Verify that the "nginx" default page is accessible on your host machine at http://localhost:8080   
    - docker ps
 - Create a new Docker container using the "httpd" image and connect it to the "my_network" network. Name the container "httpd_container".
    -   docker pull httpd
    -   docker run --name httpd_container --network my_network -d httpd
 - Verify that the "httpd" default page is accessible on your host machine at http://localhost:8081.   
    - docker ps
 -  Use the "docker network inspect" command to display information about the "my_network" network. Document your findings in the README.md file.
    - docker network inspect my_network > README.md
 - Stop and remove the "nginx_container" container
    - docker stop nginx_container
    - docker rm nginx_container
 - Create a new Docker container using the "nginx" image and connect it to the "my_network" network. Name the container "nginx_container_2"
    - docker run --name nginx_container_2 --network my_network -d nginx
 -  Verify that the "nginx" default page is accessible on your host machine at http://localhost:8082.
    - docker ps   
 - Use the "docker container ls" command to display information about all running containers. Document your findings in the README.md file
    - docker container ls > README.md
 - Stop and remove all containers. 
    - docker stop $(docker ps -a -q)
    - docker rm $(docker ps -aq)

   
