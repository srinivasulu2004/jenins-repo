# Jenkins Docker Deployment Example

This project demonstrates a basic CI/CD pipeline using:

- GitHub (source control)
- Jenkins (build server)
- Docker (deployment)

## Files

- `index.html`: Simple static webpage.
- `Dockerfile`: Builds a Docker image using NGINX.
- `Jenkinsfile`: Declarative pipeline for Jenkins.

## Build & Run

```bash
docker build -t myapp .
docker run -d -p 8080:80 myapp
```

Then visit: http://localhost:8080
