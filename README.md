# Devops Project - Java Maven App

A simple Java application built with Maven and packaged as a Docker container.

---

## Requirements

* Java 17
* Maven 3.x
* Docker (if running as a container)

---

## Build the Project

Clone the repository:

```bash
git clone <repository_url>
cd my-java-app
```

Build the JAR with Maven:

```bash
mvn clean package
```

The executable JAR will be created in the `target/` directory.

---

## Run Locally

```bash
java -jar target/my-java-app-1.0.0-jar-with-dependencies.jar
```

The application will start and listen on port `8080` by default.

---

## Docker

### Build Docker Image

```bash
docker build -t my-java-app .
```

### Run Docker Container

```bash
docker run -d --name my-java-app -p 8080:8080 my-java-app
```

### Verify

```bash
docker ps
curl http://localhost:8080
```

---

## Notes

* Make sure the JAR file has a valid `Main-Class` manifest attribute.
* If deploying to AWS ECR, configure AWS CLI and login before pushing or pulling the image.
* Update the `pom.xml` with the correct main class if needed.

---

## License

MIT License
