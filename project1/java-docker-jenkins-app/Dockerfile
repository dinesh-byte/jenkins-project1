FROM openjdk:11-jre-slim
WORKDIR /app
COPY target/java-docker-jenkins-app-1.0.0.jar app.jar
ENTRYPOINT ["java","-jar","/app.jar"]
EXPOSE 9090