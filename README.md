# Jenkins DinD (Docker in Docker)

[![](https://dockerbuildbadges.quelltext.eu/status.svg?organization=niccokunzmann&repository=dockerhub-build-status-image)](https://hub.docker.com/r/jainishshah17/jenkins-docker/builds/) 


This Jenkins Docker image provides Docker inside itself, which allows you to run any Docker container in your Jenkins build script.

Because Docker container proivdes an isolated environment for running applications or tasks, which is perfect for any CI solution. This image is designed to run everything with Docker, so it doesn't pre-install any execution environment for any specific programming language. Instead, simply run the images you need from the public Docker Hub or your private Docker registry for your CI tasks.

Run it with mounted directory from host:

```
docker run --name jenkins-dind --privileged -d -p 8080:8080 -e DOCKER_DAEMON_ARGS="--insecure-registry 0.0.0.0/0" -v /your/path:/var/lib/jenkins jainishshah17/jenkins-docker
```
