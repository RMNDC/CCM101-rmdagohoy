
# Laboratory 8: Cloud Security Engineer

## Mission Overview

Congratulations! Your proactive approach to system monitoring has earned you a spot on the elite 
Cloud Security Team at CloudNova Technologies. 
In the cloud, leaving a server unsecured for even a few minutes can lead to automated brute-force 
attacks and data breaches. Your mission today applies the security concepts you learned in Chapter 8. You will 
implement the principle of defense in depth by locking down a live server using a host-based firewall. 
Using the KillerCoda Playground, you will step into the role of a Cloud Security Engineer. You will 
deploy a web application, audit the server's open ports, and configure the Uncomplicated Firewall (UFW) to block 
malicious traffic while allowing legitimate users to access the application. 
Remember: Security is not a product you buy; it is a continuous process you maintain.

## Objectives

- Understand the Attack Surface and the Principle of Least Privilege (PoLP)
- Perform a basic security audit of active network ports on a Linux server
- Configure UFW with a Default Deny policy
- Implement granular port management to allow SSH and HTTP traffic
- Document firewall rules and security best practices using Markdown
- Continue expanding my GitHub Cloud Computing Portfolio

## Commands Executed

# Deploy the web application
docker run -d --name secure-web-app -p 8080:80 nginx
curl localhost:8080

# Build the firewall
sudo ufw allow ssh
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw enable
sudo ufw status verbose

# Allow the web application port
sudo ufw allow 8080/tcp
sudo ufw status numbered
curl localhost:8080

## Skills Learned

I learned how to turn on UFW, check its status (sudo ufw status), and create basic network rules on an Ubuntu server.  
I learned that I must allow SSH (sudo ufw allow ssh) before enabling the firewall so I don't accidentally lock myself out of my server.   
I learned how to block all incoming traffic by default and only open specific ports (like 8080/tcp) to make my server more secure.  
I learned how to run an Nginx web app inside Docker (docker run -d -p 8080:80 nginx) and test if it works using the curl command.   
