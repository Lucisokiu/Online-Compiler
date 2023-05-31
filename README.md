# Online-Compiler

sudo apt-get update

sudo apt-get upgrade

sudo apt-get install \
	 apt-transport-https \
 	ca-certificates \
 	curl \
 	gnupg-agent \
 	software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo apt-get install docker-ce docker-ce-cli containerd.io

apt-cache madison docker-ce

sudo apt-get install docker-ce docker-ce-cli containerd.io

sudo apt install docker.io

sudo apt install docker-compose

docker pull 19110455/cloud:1.2

docker run -it -p 8080:80 --name compiler -d 19110455/cloud:1.2


git clone	https://github.com/Luciferidabet/web-code_DTDM
cd web-code_DTDM

cd server

sudo usermod -a -G docker ubuntu
newgrp docker

docker build -t online-compiler .


docker run -p 8080:80 online-compiler

sudo docker-compose build 
sudo docker-compose up
