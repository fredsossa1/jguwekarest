# JGU WEKA Rest Service

Here is a summary of the commands to run to start a Docker container with the Weka Rest service.

## Prerequisites
- Installation of Docker
- Installation of Maven
- Installation of Docker-Compose

## Installing the images
```
$ mvn clean package
$ docker pull mongo
$ docker build -t weka .
```

## Installation and startup of Weka Rest
```
$ docker-compose up
```

You can now access the Swagger interface of Weka Rest via this [http: // localhost: 80] (http: // localhost: 80)
