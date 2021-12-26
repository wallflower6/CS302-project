# FROM openjdk:11
FROM maven:3.8.3-jdk-11-slim AS build
EXPOSE 8080
# WORKDIR /home/dockerdemo
# COPY ./ ./
# RUN mvn -f ./pom.xml clean package
# ADD ./target/payment-service-spring-boot.jar ./payment-service-spring-boot.jar
# ENTRYPOINT ["java", "-jar", "./payment-service-spring-boot.jar"]
ADD target/payment-service-spring-boot.jar payment-service-spring-boot.jar
ENTRYPOINT ["java", "-jar", "-Dspring.profiles.active=dev", "/payment-service-spring-boot.jar"]
