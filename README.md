# jenkins_pipeline


https://digitalavenue.dev/Run-Jenkins-On-Docker-Compose/

sudo docker container run --name jenkins-server --detach --restart unless-stopped --network jenkins-net --hostname jenkins --publish 8080:8080 --volume jenkins-data:/var/jenkins_home jenkins/jenkins:lts


