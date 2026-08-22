# Docker Installation on Linux server

## Debian-based Linux
### Check & install dependencies
```bash
dpkg -s ca-certificates curl  
```
```bash
apt update  
sudo apt install ca-certificates  
sudo apt install curl
```
### Installation
```bash
sudo install -m 0755 -d /etc/apt/keyrings  
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc  
sudo chmod a+r /etc/apt/keyrings/docker.asc  
```
```bash
sudo apt update  
sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
## RedHat-based Linux
### Check & install dependencies
```bash
rpm -q ca-certificates curl
```
```bash
dnf check-update  
sudo dnf install ca-certificates  
sudo dnf install curl
```
### Installation
```bash
sudo dnf config-manager addrepo --from-repofile https://download.docker.com/linux/fedora/docker-ce.repo  
```
```bash
sudo dnf install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin  
```
# Check/Start/enable
```bash
docker --version
docker compose version
```
```bash
sudo systemctl status docker
```
```bash
sudo systemctl enable --now docker  
```

# Test
```bash
docker info
```
Run docker container by specifying the exact registry/library/image  
```bash
sudo docker run docker.io/library/hello-world
```
If you just type the image name, Docker will search for the image in default registry (Local cache/Docker Hub)   
```bash
sudo docker run hello-word
```
