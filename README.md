# TPJavaPipeLine

A small Java Maven project built by a Jenkins declarative pipeline ([`Jenkinsfile`](Jenkinsfile)).

## Pipeline

The pipeline runs in a Docker agent (`my-maven-git:latest`, an image with Maven and Git) and mounts
`~/.m2`, so the Maven cache is reused between builds.

| Stage | What it does |
|---|---|
| Checkout | Cleans the workspace and clones this repository |
| Build & Test | `mvn clean test package` |
| Run | `java -jar target/maven-0.0.1-SNAPSHOT.jar` |

Screenshots of the builds and of the Blue Ocean view are in [`Images/`](Images). The full report,
in French, is in [REPORT.md](REPORT.md).

## Run it locally

```bash
mvn clean package
java -jar target/maven-0.0.1-SNAPSHOT.jar
```

It prints `Hello DevOps & Cloud Computing`.
