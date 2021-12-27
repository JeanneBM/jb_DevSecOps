## Init
```
vagrant init centos/7
vagrant up
vagrant ssh

vagrant ssh-config >> C:/Users/ ... /.ssh/config

# /usr/bin/ssh init@127.0.0.1 -p 2222

sudo yum upgrade; sudo yum install -y vim; sudo yum install -y net-tools 
```

## Static IP
https://www.itzgeek.com/how-tos/linux/centos-how-tos/how-to-configure-static-ip-address-in-centos-7-rhel-7-fedora-26.html


## Partition
```
lsblk; df -h
fdisk /dev/sda 
```
## Docker CE on CentOS:
```
sudo yum install -y yum-utils; sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo; sudo yum install docker-ce docker-ce-cli containerd.io; yum list docker-ce --showduplicates | sort -r; sudo yum install docker-ce-<VERSION_STRING> docker-ce-cli-<VERSION_STRING> containerd.io; sudo systemctl start docker; sudo docker run hello-world
docker version
sudo groupadd docker; sudo usermod -aG docker $USER; sudo reboot ; [after reboot] systemctl start docker; sudo systemctl status docker
```
## Jenkins:
```
sudo yum install -y wget; sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo; sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key; sudo yum upgrade; sudo yum install -y epel-release java-11-openjdk-devel; sudo yum install -y jenkins; sudo systemctl daemon-reload; sudo systemctl start jenkins; sudo systemctl enable jenkins; sudo systemctl status jenkins


```

## Git
```
vim Dockerfile
docker build -t git .
```

## Docker_env


