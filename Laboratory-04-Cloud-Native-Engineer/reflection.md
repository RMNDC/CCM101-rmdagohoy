## Mission Overview
Congratulations! After successfully guiding our clients through multi-cloud evaluations, you have been promoted to the Cloud-Native Engineering Team at CloudNova Technologies. 
Modern cloud computing is no longer just about renting Virtual Machines (VMs) from AWS or Azure. Today's enterprise applications are built using lightweight, portable, and lightning-fast technologies called Containers. Your new mission is to understand the shift from traditional virtualization to containerization. 
Using the KillerCoda Playground, you will step into the shoes of a Cloud-Native Engineer. You will research the differences between VMs and containers, execute your very first Docker commands, and deploy a live, containerized web server in seconds. Remember: A traditional system administrator manages servers, but a cloud-native engineer manages the services running on them.

## Mission Objectives
At the end of this laboratory activity, you should be able to:
* Differentiate between traditional Virtual Machines (VMs) and Containers.
* Access a Docker-enabled cloud environment using KillerCoda.
* Execute fundamental Docker CLI (Command Line Interface) commands.
* Pull, run, manage, and terminate a containerized application (Nginx).
* Create professional technical documentation of container operations using Markdown.
* Continue developing a well-organized GitHub Cloud Computing Portfolio.

## Docker Commands Executed

### Checkpoint 3 — Environment Setup & Verification
* `docker --version`: Checks the installed Docker client version on the host system.
* `docker info`: Displays system-wide information regarding the Docker installation.

### Checkpoint 4 — Pulling and Running NGINX
* `docker pull nginx`: Downloads the official NGINX image from Docker Hub to the local repository.
* `docker run -d -p 8080:80 --name my-nginx nginx`: Deploys the NGINX container in detached mode (`-d`), assigns it the name `my-nginx`, and maps port 8080 on the host to port 80 inside the container.
* `curl http://localhost:8080`: Sends an HTTP request to verify that the NGINX web server is active and serving traffic. 

### Checkpoint 5 — Container Lifecycle Management
* `docker ps`: Lists all currently active and running containers.
* `docker stop my-nginx`: Gracefully halts the execution of the running `my-nginx` container.
* `docker ps -a`: Lists all containers (including stopped/exited ones) to verify that `my-nginx` has stopped.
* `docker rm my-nginx`: Permanently deletes the stopped `my-nginx` container from the system.

## Skills Learned
* Containers vs. VMs: Understood why containers are lighter and faster than Virtual Machines because they share the main host system instead of running a full guest OS.

* Basic Docker Commands: Learned how to download images, start containers, check running processes, and clean up container instances using the Docker CLI.

* Port Mapping: Learned how to map ports so network traffic can travel from my machine into a containerized application like NGINX.

* Managing Container Lifecycle: Got hands-on experience starting, stopping, checking, and deleting temporary containers without leaving messy files behind.

## Challenges Encountered
* Understanding Port Syntax: It took a minute to remember that -p 8080:80 maps the host port first and the container port second.

* Checking Container Status: Remembering to run docker ps -a instead of regular docker ps to verify that a container actually stopped before removing it.
