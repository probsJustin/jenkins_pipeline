# jenkins_pipeline


https://digitalavenue.dev/Run-Jenkins-On-Docker-Compose/

sudo docker container run --name jenkins-server --detach --restart unless-stopped --network jenkins-net --hostname jenkins --publish 8080:8080 --volume jenkins-data:/var/jenkins_home jenkins/jenkins:lts


http://<DOCKER-HOST-IP>:8080/
  
  172.105.156.21

http://172.105.156.21:8080/
