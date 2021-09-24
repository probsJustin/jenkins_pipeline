# Multi-User Jenkins Pipeline: 
## Current Build Status: 
[![Build Status](http://172.105.156.21:8080/buildStatus/icon?job=jenkins_pipeline_test_build)](http://172.105.156.21:8080/job/jenkins_pipeline_test_build/)
## About: 
Multi purepose pipeline for doing github linked builds with multiple users 

## Rules: 
- Application must be self contained (meaning it needs to be containerized and can only store files locally to that container) 
- Application can not leave any dirt behind on the system (meaning please remove your container images in the clean up of your jenkins pipeline) 

## How to: 
**How to set up your own build/deployment with github:
https://medium.com/@koen.vantomme/how-to-integrate-your-github-repository-to-your-jenkins-project-802168ad1777

How to get your own build status in your readme: 
https://www.vegait.rs/media-center/blog/how-to-display-jenkins-build-status-badge-on-github

## Notes for setting up persisted jekins pipeline
>>>>>>> 15685f0f10aec2ab6e11ef2e5484a58ab85ec0f4
https://digitalavenue.dev/Run-Jenkins-On-Docker-Compose/

mkdir /var/jenkins_home 

sudo docker container run --name jenkins-server --detach --restart unless-stopped --network jenkins-net --hostname jenkins --publish 8080:8080 --volume jenkins-data:/var/jenkins_home jenkins/jenkins:lts



sudo docker container run --detach --restart unless-stopped --network jenkins-net --hostname jenkins --publish 8080:8080 --volume jenkins-data:/var/jenkins_home jenkins/jenkins:lts


Running from: /usr/share/jenkins/jenkins.war
webroot: EnvVars.masterEnvVars.get("JENKINS_HOME")
Exception in thread "main" java.lang.reflect.InvocationTargetException
        at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
