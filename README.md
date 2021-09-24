# Multi-User Jenkins Pipeline: 


## About: 
## Rules: 
- Application must be self contained (meaning it needs to be containerized and can only store files locally to that container) 
- Application can not leave any dirt behind on the system (meaning please remove your container images in the clean up of your jenkins pipeline) 

## How to: 
**How to set up your own build/deployment with github:
https://medium.com/@koen.vantomme/how-to-integrate-your-github-repository-to-your-jenkins-project-802168ad1777


## Notes for setting up persisted jekins pipeline
https://digitalavenue.dev/Run-Jenkins-On-Docker-Compose/

mkdir /var/jenkins_home 

sudo docker container run --name jenkins-server --detach --restart unless-stopped --network jenkins-net --hostname jenkins --publish 8080:8080 --volume jenkins-data:/var/jenkins_home jenkins/jenkins:lts

http://172.105.156.21:8080/
