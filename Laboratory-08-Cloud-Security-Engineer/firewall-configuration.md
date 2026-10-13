# Firewall Configuration

## 1. Allow SSH

sudo ufw allow ssh

## 2. Set the Default Deny Policy

sudo ufw default deny incoming
sudo ufw default allow outgoing

## 3. Allow Port 8080

sudo ufw allow 8080/tcp

##
If we enable the firewall remotely before allowing SSH, the connection will drop instantly and it will be locked out of our server.
