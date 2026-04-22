FROM openjdk:11-jre-slim
VOLUME /tmp
COPY target/java-docker-jenkins-app.jar app.jar
ENTRYPOINT ["java","-jar","/app.jar"]
EXPOSE 9090