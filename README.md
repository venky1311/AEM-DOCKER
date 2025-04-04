# AEM Docker Setup

This README provides detailed instructions for setting up Adobe Experience Manager (AEM) author and publisher instances using Docker. Follow these steps to build and run your AEM instances locally# AEM Docker Setup

## Prerequisites

- **Docker**: Ensure Docker is installed and running on your machine. You can download Docker from [Docker's official website](https://www.docker.com/products/docker-desktop).
- **AEM SDK**: Download the AEM as a Cloud Service SDK, which includes the necessary JAR files and license properties.

## Directory Structure

```plaintext
- aem-docker
  - author
    - [Dockerfile](aem-docker/author/Dockerfile)
    - aem-author-p4502.jar ** Please place the jar and rename
    - license.properties ** for cloud sdk is not required
  - publisher
    - [Dockerfile](aem-docker/publisher/Dockerfile)
    - aem-publish-p4503.jar ** Please place the jar and rename
    - license.properties
  - dispatcher
    - [Dockerfile](aem-docker/dispatcher/Dockerfile)
    - dispatcher.any
    - httpd.conf
.

## Prerequisites

- **Docker**: Ensure Docker is installed and running on your machine. You can download Docker from [Docker's official website](https://www.docker.com/products/docker-desktop).
- **AEM SDK**: Download the AEM as a Cloud Service SDK, which includes the necessary JAR files and license properties.

## Directory Structure

```plaintext
- aem-docker
  - author
    - Dockerfile
    - aem-author-p4502.jar
    - license.properties
  - publisher
    - Dockerfile
    - aem-publish-p4503.jar
    - license.properties
  - dispatcher
    - Dockerfile
    - dispatcher.any
    - httpd.conf
```

## Setup Instructions

## Author Instance
1. Navigate to the Author Directory:
   Open your terminal and navigate to the author directory:
   
   cd aem-docker/author

2. Build the Docker Image:
   Build the Docker image for the author instance:

   docker build -t aem-author:latest .

3. Run the Docker Container:
   Run the Docker container for the author instance:

   docker run -d -p 4502:4502 --name aem-author aem-author:latest

4. Access the Author Instance:
   Open your browser and navigate to http://localhost:4502 to access the AEM author instance.

## Publisher Instance

1. Navigate to the Publisher Directory:
   Open your terminal and navigate to the publisher directory:
   
   cd aem-docker/publisher

2. Build the Docker Image:
   Build the Docker image for the author instance:

   docker build -t aem-publisher:latest .

3. Run the Docker Container:
   Run the Docker container for the publisher instance:

   docker run -d -p 4503:4503 --name aem-publisher aem-publisher:latest

4. Access the Publisher Instance:
   Open your browser and navigate to http://localhost:4503 to access the AEM publisher instance.

## Dispatcher Setup

1. Navigate to the Dispatcher Directory:
   Open your terminal and navigate to the dispatcher directory:
   
   cd aem-docker/dispatcher

2. Build the Docker Image:
   Build the Docker image for the dispatcher:

   docker build -t aem-dispatcher:latest .

4. Run the Docker Container:
   Run the Docker container for the dispatcher:
   
   docker run -d -p 80:80 --name aem-dispatcher aem-dispatcher:latest

5. Access the Dispatcher:

Open your browser and navigate to http://localhost to access the dispatcher.

# Docker-compose

First time run you can use for starting => docker-compose up
For stopping => docker-compose down


Easiest way to start and stop the containers
# docker stop aem-dispatcher aem-publisher aem-author
# docker start aem-dispatcher aem-publisher aem-author


