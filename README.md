docker build -t helloapp .

docker run helloapp

----------------------------------

Hello.java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello from Docker Container!");
    }
}

Dockerfile
FROM openjdk:17
WORKDIR /app
COPY Hello.java .
RUN javac Hello.java
CMD ["java", "Hello"]

Build & Run
docker build -t helloapp .
docker run helloapp


✔ Output displayed correctly
