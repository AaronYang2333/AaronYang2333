---
title: install docker and docker-compose on Ubuntu
catalog: true
mathjax: true
date: 2021-04-01 02:28:45
subtitle:
header-img:
tags:
- Docker
- Docker Compose
- Ubuntu
categories:
- Docker
---

#### Install Docker and remove old version Docker
```shell
sudo apt-get remove docker docker-engine docker.io
```

#### Add Docker Repository

```shell
sudo apt-get update
sudo apt-get install apt-transport-https ca-certificates  curl software-properties-common
curl -fsSL https://mirrors.ustc.edu.cn/docker-ce/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://mirrors.ustc.edu.cn/docker-ce/linux/ubuntu $(lsb_release -cs) stable"
```

#### Install Docker CE（Community Version）

```shell
sudo apt-get update -y
sudo apt-get install docker-ce -y
```

#### Startup when boot
```shell
sudo systemctl enable docker
sudo systemctl start docker
```

#### Add current user into Docker group
```shell
sudo groupadd docker
sudo usermod -aG docker $USER
```

#### Test Installation
```shell
docker run hello-world
```

#### Use China Official Image (if you need)

use <b>vim /etc/docker/daemon.json</b>, and then append this content into the file
```json
{
   "registry-mirrors": [
     "https://registry.docker-cn.com"
   ]
 }
 
```

#### Restart docker

```shell
sudo systemctl daemon-reload
sudo systemctl restart docker
```

#### Install Docker Compose
```shell
sudo curl -L https://github.com/docker/compose/releases/download/1.18.0/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose --version
```

#### Install auto-complete plugin


```shell
curl -L https://raw.githubusercontent.com/docker/compose/1.8.0/contrib/completion/bash/docker-compose > /etc/bash_completion.d/docker-compose
```