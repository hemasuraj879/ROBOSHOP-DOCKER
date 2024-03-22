# Use an official Maven image as the base image
FROM maven:3.8.4-openjdk-17 AS build

# Set the working directory in the container
WORKDIR /app

# Copy the Maven project's POM and source code
COPY pom.xml .
COPY src ./src

# DEPENDENCY RESOLVING
RUN mvn dependency:resolve

# Build the Maven project
RUN mvn clean package



# Use a lightweight OpenJDK image as the base image for runtime
FROM  openjdk:8-jre-alpine3.9

# Exposing this application on specific port
EXPOSE 8080

# Setting up environment variables
ENV CART_ENDPOINT=cart:8080
ENV DB_HOST=mysql

# Set the working directory in the container
WORKDIR /app

# Copy the built JAR file from the build stage
COPY --from=build /app/target/shipping-1.0.jar shipping.jar

# Specify the command to run your application
CMD ["java", "-jar", "shipping.jar"]