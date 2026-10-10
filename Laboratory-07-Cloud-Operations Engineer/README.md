# Mission Overview
Congratulations! Your ability to deploy multi-tier architectures has proven your technical capabilities. 
You have now been promoted to the Cloud Operations Team (often referred to in the industry as Site Reliability 
Engineering, or SRE) at CloudNova Technologies. 
Deploying a cloud application is only the first step; keeping it running smoothly is the real challenge. 
When a server crashes or a web page takes ten seconds to load, you cannot simply guess what is wrong. You 
must rely on Observability and Monitoring to see inside your infrastructure. 
Using the KillerCoda Playground, you will step into the role of a Cloud Operations Engineer. You will 
establish a performance baseline for your Linux server, deploy a containerized application, generate artificial web 
traffic, and hunt down performance metrics and system logs to prove the application is healthy. 
Remember: A developer hopes the application works; a Site Reliability Engineer uses metrics and logs to 
prove it. 

# Mission Objectives 
At the end of this laboratory activity, you should be able to: 
 Utilize native Linux command-line tools to monitor host CPU, Memory, and Disk capacity. 
 Deploy a web container and track its real-time performance using Docker metrics. 
 Generate web traffic and extract application access logs for analysis. 
 Translate raw performance data into a readable technical report using Markdown. 
 Continue expanding a professional GitHub Cloud Computing Portfolio. 

# Monitoring Commands Executed

Command 
- free -h
- df -h
- top 
- docker --versio
- docker run -d --name client-website -p 8080:80 nginx
- docker ps
- curl http://localhost:8080
- curl http://localhost:8080/hidden-admin-page
- docker logs client-website
- docker stats
- docker rm -f client-website

# Skills Learned

- I learned how to check the server's available RAM and disk space so I can make sure it won't crash when traffic surges.
- I learned that mapping port 8080:80 forwards traffic from port 8080 on the host machine to port 80 inside the container so users can access the website.
- I learned how to test site pages, seeing that an HTTP 200 means the request succeeded while an HTTP 404 means the page was not found.
- I learned how to test site pages, seeing that an HTTP 200 means the request succeeded while an HTTP 404 means the page was not found.
