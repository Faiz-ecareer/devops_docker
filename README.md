# devops_docker
Docker projects as part of my DevOps journey.  

# Docker Installation on Linux server

## Debian-based Linux
### Check & install dependencies
dpkg -s ca-certificates curl    
apt update  
sudo apt install ca-certificates  
sudo apt install curl  
### Installation
sudo install -m 0755 -d /etc/apt/keyrings  
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc  
sudo chmod a+r /etc/apt/keyrings/docker.asc  

sudo apt update  

sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin  

## RedHat-based Linux
### Check & install dependencies
rpm -q ca-certificates curl    
dnf check-update  
sudo dnf install ca-certificates  
sudo dnf install curl  
### Installation
sudo dnf config-manager addrepo --from-repofile https://download.docker.com/linux/fedora/docker-ce.repo  

sudo dnf install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin  

# Check/Start/enable
docker --version  
sudo systemctl status docker  
sudo systemctl enable --now docker  

