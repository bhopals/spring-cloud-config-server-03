# Introduction
 Spring Microservices 

The Spring Cloud Config service and how you can use it managed the configuration of your microservices. 

1.  A Spring Cloud Config server that is deployed as Docker container and can manage a services configuration information using a file system or GitHub-based repository.
2.  A organization service that will manage organization data used within EagleEye.
3.  A licensing service that will manage licensing data used within EagleEye.
4.  A Postgres SQL database used to hold the data for these two services.

# Software needed
1.	Apache Maven (http://maven.apache.org)
2.	Docker (http://docker.com)
3.	Git Client (http://git-scm.com)

# Building the Docker Images 

Run the following maven command.  

   **mvn clean package docker:build**

If everything builds successfully you should see a message indicating that the build was successful.

# Running the services

Now we are going to use docker-compose to start the actual image.  To start the docker image, issue the following docker-compose command:

   **docker-compose -f docker/common/docker-compose.yml up**

If everything starts correctly you should see a bunch of Spring Boot information fly by on standard out.  