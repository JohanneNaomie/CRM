# Use an official Maven image to build the app
FROM maven:3.8.4-openjdk-17-slim AS builder

# Set the working directory inside the container
WORKDIR /app

# Copy the pom.xml and the src directory into the container
COPY pom.xml .
COPY src ./src

# Build the Spring Boot application
RUN mvn clean package -DskipTests -X


# Inspect the /app/target directory after build
RUN ls -l /app/target
