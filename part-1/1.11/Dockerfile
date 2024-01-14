FROM openjdk:11

WORKDIR /usr/src/myapp

COPY . /usr/src/myapp

RUN ./mvnw package

EXPOSE 8080

CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]

# Opens a page with a button that says "press here", when you click it, it says "success"