# DockerInstallationOnWSL
Installation instructions for docker on Ubuntu and Centos/Rocky Linux.

Ubuntu:
```bash
curl -fsSL https://get.docker.com -o install-docker.sh
sudo apt install podman-docker
sh install-docker.sh
sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker
```

CentOS/Rocky:
```bash
sudo dnf config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
sudo dnf install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y
sudo systemctl start docker
sudo systemctl enable docker
sudo usermod -aG docker $USER
```
