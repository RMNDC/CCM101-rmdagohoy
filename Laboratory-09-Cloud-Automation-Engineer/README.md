# Laboratory 9: Cloud Automation Engineer

## Mission Overview

Congratulations! Your ability to secure cloud environments has proven you are ready for the highest 
level of operations. You have been promoted to the Cloud Automation and DevOps Team at CloudNova 
Technologies. 
Up until now, you have been acting as a traditional systems administrator—typing commands manually 
one by one. In large enterprise environments scaling to thousands of servers, manual administration is too slow 
and highly prone to human error. To survive at scale, you must learn to automate. 
Using the KillerCoda Playground, you will step into the role of a Cloud Automation Engineer. You will 
learn the basics of Bash shell scripting, create an automated backup routine, assign executable permissions, and 
configure the Linux Cron scheduler to run your code autonomously. 
Remember: If you have to do a task more than twice in the cloud, you should automate it. 
## Objectives

- Understand the syntax of a Bash script, including variables and basic commands
- Use nano to write and save scripts
- Modify Linux file permissions using chmod
- Understand task scheduling and the crontab syntax
- Document automation code and cron configurations in Markdown
- Complete my GitHub Cloud Computing Portfolio

## Commands Executed


mkdir app-data
echo "This is critical client data." > app-data/data.txt
nano backup.sh
./backup.sh
chmod +x backup.sh
./backup.sh
ls -l backups/
crontab -l
env EDITOR=nano crontab -e
crontab -l


## Skills Learned

I learned how to write and save shell scripts using nano to automate repetitive tasks like creating directories and compressing files into backups.  
I learned how to use chmod +x to grant execute permissions, fixing the "Permission denied" error so custom scripts can run properly. 
I learned how to use the Linux crontab scheduler to run automated scripts on a strict schedule in the background without needing manual supervision.   

