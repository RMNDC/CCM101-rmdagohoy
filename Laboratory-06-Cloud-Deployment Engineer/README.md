# Mission Overview
Congratulations! Your flawless work in deploying data storage solutions has earned you a spot on the 
Cloud Deployment Team at CloudNova Technologies. 
Up until now, you have been deploying single containers (like a standalone web server or a storage 
bucket). However, real-world enterprise applications are rarely just one container. They are "multi-tier" systems 
that require a frontend web application communicating seamlessly with a backend database. Deploying these 
one by one manually is prone to error. 
Enter Docker Compose. In this mission, you will transition from manual commands to Infrastructure 
as Code (IaC). Using a YAML configuration file, you will define a multi-container private cloud storage application 
(Nextcloud and MariaDB) and deploy the entire stack simultaneously with a single command! 
Remember: A junior engineer deploys servers by typing commands; a senior engineer deploys 
infrastructure by writing code.

# Objectives 
At the end of this laboratory activity, you should be able to: 
- Explain the concept of a multi-tier application architecture. 
- Understand the purpose and structure of a docker-compose.yml file. 
- Use a Linux command-line text editor (nano) to create configuration files. 
- Deploy a multi-container application (Nextcloud + Database) using Docker Compose. 
- Document deployment procedures and Infrastructure as Code (IaC) principles using Markdown. 
- Continue expanding your professional GitHub Cloud Computing Portfolio. 

# Commands Executed 

-mkdir nextcloud-deployment

-cd nextcloud-deployment

-nano docker-compose.yml

-cat docker-compose.yml

-docker-compose up -d

-docker-compose ps

-docker-compose down


# Skills Learned

- Using `nano` to create and edit configuration files from the command line
- Understanding two-tier architecture: a web/application tier and a database tier
- Passing configuration to containers with environment variables
- Mapping ports (`8080:80`) to reach an app in a container from the browser
- Verifying and tearing down a stack with `docker-compose ps` and `docker-compose down`
- Documenting infrastructure as code (IaC) in Markdown
