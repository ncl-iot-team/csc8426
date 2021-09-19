# CSC8426: Emerging Technologies - Docker Platform
This repository contains essential materials and references for the practicals of CSC8426 Emerging Technologies module. Please read https://docs.docker.com/engine/docker-overview/ before doing the exercises.
## Tutorial Videos
### Pre VirtualBox Tutorial
https://bit.ly/3lxcmzi

### Task1 Emerging Technologies Coursework
https://bit.ly/3tQndbs

### Introduction to Docker Swarm
https://bit.ly/3Er3Zy9

### Docker Build Toturial 
https://bit.ly/3Cr2Sg1

### Introduction to cAdvisor
https://bit.ly/2XxhnAg


## Pre-Requsities Installation
### Virtual Machine with Docker Pre-Installed   (Recommended)
Docker environment run seamlessly in Linux. It is recommended using the provided Virtual Machine Linux Image. Follow the below steps to setup a VM environment in your local machine.

1. Download and install virtual box https://www.virtualbox.org/wiki/Downloads

2. Download Virtual Machine Image (with Docker Pre-Installed): https://bit.ly/3hML1rZ

3. Import and run the ova file using VirtualBox. Username and password are cloud/cloud

If you have already installed Docker for Windows, existing installation and related feature (Hyper-V) may create conflicts while running a VM image. Please disable Hyper-V, Virtual Machine Platform, Windows Hypervisor Platform, Windows Sandbox, Windows Subsystem for Linux and restart windows before running VirtualBox


![Disable HyperV Step 1](disableHyper-V-1.png?raw=true "Search for 'Turn Windows Features on or off'")
![Disable HyperV Step 2](disable-HyperV.png?raw=true "Disable Hyper-V")


## Explanation References
### Container Introduction
https://www.youtube.com/watch?v=EnJ7qX9fkcU

### Docker Swarm Intro
https://www.youtube.com/watch?v=Tm0Q5zr3FL4
Refer https://docs.docker.com/engine/swarm/ for basic concepts

### Docker Engine SDK and API
Docker provides an API for interacting with the Docker daemon (called the Docker Engine API), as well as SDKs for Go and Python. There are unofficial libraries for other programming languages. If you choose to use Java as your programming language, you may use https://github.com/spotify/docker-client. Unofficial libraries don't come with all the features. Some provide control over basic docker engine features only.

The SDKs allow you to build and scale Docker apps and solutions quickly and easily. If Go or Python won’t work for you, you can use the Docker Engine API directly or any other language third-party SDKs for 

The Docker Engine API is a RESTful API accessed by an HTTP client such as wget or curl, or the HTTP library which is part of most modern programming languages.

Refer https://docs.docker.com/develop/sdk/

Python SDK Reference : https://docker-py.readthedocs.io/en/stable/

###  locustio/locust
1. Basic features
	https://github.com/locustio/locust
1. Running in Docker
	https://docs.locust.io/en/stable/running-locust-docker.html
	
###  Mongo Database
1. Official Website
	https://www.mongodb.com
1. Docker QuickStart
	https://hub.docker.com/_/mongo

### Google cAdvisor Remote REST API Reference
1. Pattern of API endpoint
    http://&lt;hostname&gt;:&lt;port&gt;/api/&lt;version&gt;/&lt;request&gt;
    
    The current version of the API is v1.3 and there is a beta release of the v2.0 API
    
    Supported request types: &quot;containers,docker,events,machine,subcontainers&quot;
    
    Example http://localhost:8888/api/v1.3/containers
    The result is returned in JSON format.
2. To get information of all sub containers http://localhost:8888/api/v1.3/subcontainers/
3. To get information of a specific sub container http://localhost:8888/api/v1.3/subcontainers/&lt;subcontainername&gt;

#### Example 1. To get information of all sub-containers within docker container
    http://localhost:8888/api/v1.3/subcontainers/docker
#### Example 2. To get information of a container within docker container
    http://localhost:8888/api/v1.3/subcontainers/docker/497cec18b8114c2ecdda1efb87f7795c594d7b431a59d5c775390426093b9631
    Containers’ name are available from the endpoint
    http://localhost:8888/api/v1.3/subcontainers or
    http://localhost:8888/api/v1.3/subcontainers/docker

Reference
https://github.com/google/cadvisor/blob/master/docs/api.md

### Docker Swarm Visualizer
Refer: https://github.com/dockersamples/docker-swarm-visualizer

Also Refer the docker-compose.yml file in https://docs.docker.com/get-started/part5/#add-a-new-service-and-redeploy 

## FAQ
1. **Tips for Task 1 - Deploy a web application component in Docker Environmen**

    It is a basic docker job which has to be performed using Command line (Refer https://docs.docker.com/get-started/part2/#run-the-app)

    
2. **Tips for Task 2 - Deploy a complex web application stack in Docker Environmentt**

    The docker compose overview and practices can be found in https://docs.docker.com/compose/ 

3. **Tips for Task 3 - Build your own Docker image and push it to the Docker Hub**

    You can download the source code of the provided Java program in this link https://github.com/ncl-iot-team/cadvisor-scraper
	Before you push the new built docker image to the remote Docker Hub repository, please don't forget to login with your Docker Hub account in command link interface, and tag your built image with "&lt;your username&gt;/&lt;image name&gt;". 

4. **Tips for Task 4 - Fully deploy and run the complex web application stack and undertakeperformance benchmarking activities**
	
	When you plan to verify the container statistics recorded in the MongoDB instance, you can try to deploy a mongodb express service, refer https://github.com/mongo-express/mongo-express which can be deployed in Docker environment, ref https://hub.docker.com/_/mongo-express/
	
