# learn-docker
create EC2 instance on AWS and install docker

#### install docker
```text
sudo dnf install docker
```
#### to install docker cd
```text
#setup repo
sudo dnf -y install dnf-plugins-core
sudo dnf config-manager --add-repo https://download.docker.com/linux/rhel/docker-ce.repo
```
#### install latest version
```text
sudo dnf install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
#### start docker engine
```text
sudo systemctl enable --now docker
sudo systemctl start docker
```
#### verify docker
```text
sudo docker run hello-world
```
#### run docker image (if not found locally it will try to download from internet)
```text
docker run nginx
```
#### to see all the containers running (note the container id)
```text
docker PS -a

#note container ip and test as following
docker docker-ip
```
#### run docker in detached mode
```text
docker run -d nginx
```
#### run docker at published port p 8080
```text
docker run -d -p 8080 nginx
```
#### map port 8080 on local server to port 80 on docker (server port:docker port)
```text
docker run -d -p 8080:80 nginx
```
#### run as root user, try these docker cmds
```text
docker run redhat/ubi9 id
```
```text
docker run -u bin redhat/ubi9 id
```
```text
docker run -u bin redhat/ubi9 id cat/etc/passwd
```
```text
docker run -e env
```
```text
#inject variable URL
docker run -e URL=google.com redhat/ubi9 env
```
#### check docker logs
```text
docker ps
#note the docker id

docker logs docker_id
#will show logs on docker container  
```
#### Deploy roboshop on docker containers
- Modify ansible code to install docker on servers and deploy roboshop on containers
- Note that DB instances are not containerized
