# Laboratory 10: Enterprise Cloud Architect

## Mission Overview 
Congratulations! You have survived the rigorous ranks of CloudNova Technologies. From a Junior Trainee learning basic Linux commands to a Cloud Automation Engineer scripting self-healing infrastructure, you have proven your technical expertise at every level. 
Your exceptional track record has caught the attention of the executive board. Cledmar Badongen, the visionary CEO of CloudNova Technologies, has personally selected you for a massive undertaking. You have been promoted to Enterprise Cloud Architect. 
For your final mission, the training wheels are completely off. There are no step-by-step instructions. You are required to design, deploy, secure, automate, and document a complete, production-ready enterprise infrastructure of your own choosing from scratch. Finally, you will prove your system works by defending it live. Remember: An Architect does not follow a manual; they write it. 

## Mission Objective
- Conceptualize and diagram a custom enterprise cloud infrastructure. 
-	Provision and configure a local Virtual Machine running a headless Linux distribution (Ubuntu Server). 
-	Install and configure Docker and Docker Compose on a fresh operating system. 
-	Deploy a multi-tier containerized application utilizing persistent data volumes without guided instructions. 
-	Implement comprehensive system security and port management independently. 
-	Automate operational tasks (such as disaster recovery or health checks) using custom Bash scripts and task scheduling. 
-	Synthesize all technical documentation into a professional GitHub Cloud Computing Portfolio. 
-	Demonstrate and defend your infrastructure live in a simulated corporate boardroom setting. 

## Command Executed
### 1. VM Setup and SSH
```bash
ip a
sudo apt-get install -y openssh-server
sudo systemctl enable --now ssh
ssh your-username@192.168.X.X
```

### 2. Docker Installation
```bash
sudo apt-get update -y
sudo apt-get install -y ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update -y
sudo apt-get install -y docker-ce docker-ce-cli containerd.io docker-compose-plugin
sudo systemctl enable --now docker
sudo usermod -aG docker $USER
exit
ssh your-username@192.168.X.X
docker ps
```

### 3. Project Setup and Deployment
```bash
mkdir -p ~/enterprise-stack
cd ~/enterprise-stack
cat > docker-compose.yml << 'EOF' ... EOF
cat docker-compose.yml
docker compose up -d
docker compose ps
```

### 4. Persistence Test
```bash
sudo reboot
ssh your-username@192.168.X.X
cd ~/enterprise-stack
docker compose ps
```

### 5. Troubleshooting
```bash
docker compose ps
docker compose logs db
docker compose logs wordpress
```

### 6. Security Hardening (UFW)
```bash
sudo apt-get install -y ufw
sudo ufw allow ssh
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow 8080/tcp
sudo ufw enable
sudo ufw status verbose
```

### 7. Docker Firewall Bypass Fix
```bash
sudo nano /etc/ufw/after.rules
sudo ufw reload
sudo iptables -L DOCKER-USER -n -v
docker run -d --rm --name fwtest -p 9090:80 nginx
docker stop fwtest
```

Rules added to the bottom of `/etc/ufw/after.rules`:

```
# BEGIN DOCKER FIREWALL FIX
*filter
:DOCKER-USER - [0:0]
-A DOCKER-USER -m conntrack --ctstate ESTABLISHED,RELATED -j RETURN
-A DOCKER-USER -i enp0s3 -p tcp -m conntrack --ctorigdstport 8080 --ctdir ORIGINAL -j RETURN
-A DOCKER-USER -i enp0s3 -j DROP
-A DOCKER-USER -j RETURN
COMMIT
# END DOCKER FIREWALL FIX
```

### 8. Backup Automation
```bash
mkdir -p ~/scripts ~/backups
cd ~/scripts
cat > backup.sh << 'EOF' ... EOF
chmod +x backup.sh
./backup.sh
ls -lh ~/backups/
realpath backup.sh
env EDITOR=nano crontab -e
crontab -l
cat ~/backups/backup.log
```

Cron job added:

```
0 2 * * * /home/your-username/scripts/backup.sh >> /home/your-username/backups/backup.log 2>&1
```

## Skills Learned
- Setting up and networking a Linux Ubuntu server in a virtual machine
- Managing a remote server through SSH using Powershell
- Installing software from third-party repositories
- Deploying multi-container applications with Docker Compose
- Securing a server with UFW and understanding how Docker bypasses it
- Using Cron for automating and Adding bash script
