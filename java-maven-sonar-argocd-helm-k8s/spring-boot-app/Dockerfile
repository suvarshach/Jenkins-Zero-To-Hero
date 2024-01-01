# base image for the Docker image. In this case, it's using the Alpine Linux variant of the AdoptOpenJDK OpenJDK 11 image.
FROM adoptopenjdk/openjdk11:alpine-jre

# Simply the artifact path
#This line defines a build argument named artifact, which represents the path to the Spring Boot application artifact (JAR file). 
#The default value is set to target/spring-boot-web.jar.
ARG artifact=target/spring-boot-web.jar

#This sets the working directory inside the container to /opt/app. Subsequent commands will be executed in this directory.
WORKDIR /opt/app
#This copies the Spring Boot application JAR file from the local build context (usually where the Dockerfile is located) to the /opt/app directory inside the container. 
The filename in the container is set to app.jar
COPY ${artifact} app.jar

# This sets the default command to run when the container starts. It specifies that the Spring Boot application should be executed using the java -jar command, 
and the JAR file to execute is app.jar
ENTRYPOINT ["java","-jar","app.jar"]
