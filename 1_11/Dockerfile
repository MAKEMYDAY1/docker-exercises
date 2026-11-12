FROM amazoncorretto:8-alpine-jdk
WORKDIR /usr/src/app
COPY .mvn .mvn/ 
COPY mvnw* pom.xml .
RUN chmod +x mvnw
RUN ./mvnw dependency:go-offline
COPY src src/
RUN ./mvnw package && rm -rf /root/.m2/repository
EXPOSE 8080
CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]
