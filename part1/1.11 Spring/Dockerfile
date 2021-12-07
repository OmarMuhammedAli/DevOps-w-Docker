FROM openjdk:8

WORKDIR /usr/src/app

COPY . .

RUN apt-get update && apt-get install -y dos2unix
RUN chmod +x mvnw
RUN dos2unix mvnw
RUN ./mvnw package

CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]

EXPOSE 8080