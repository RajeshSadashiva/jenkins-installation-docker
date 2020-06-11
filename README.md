#jenkins-installation-docker

#This page will show you how to install jenkins on docker


#Installation of Docker

sudo apt-get update

sudo apt-get install     apt-transport-https     ca-certificates     curl     gnupg-agent     software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo apt-key fingerprint 0EBFCD88

sudo add-apt-repository    "deb [arch=amd64] https://download.docker.com/linux/ubuntu \$(lsb_release -cs) \stable"

sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io


#Pulling docker Image and running

sudo docker network create jenkins

sudo docker run --name jenkinsci -p 8080:8080 jenkins/jenkins:lts

#Managing docker Image

sudo docker start <Container ID>

sudo docker pause <Container ID>

sudo docker unpause <Container ID>
