# Base image
FROM openjdk:11-jdk-slim

# Set the working directory inside the container
WORKDIR /app

# Copy the packaged Spring Boot application JAR file to the container
COPY ../../target/my-api-1.0.0.1591234567.jar  /app/app.jar

# Expose the port that your Spring Boot application listens on
EXPOSE 8080

# Set the entry point for the container to execute your Spring Boot application
ENTRYPOINT ["java", "-jar", "app.jar"]

