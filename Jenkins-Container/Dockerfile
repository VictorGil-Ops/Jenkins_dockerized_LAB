# Dockerfile Jenkins with docker installed
# https://download.docker.com/linux/

FROM jenkins/jenkins:latest

USER root
RUN apt-get update -qq \
    && apt-get install -qqy apt-transport-https ca-certificates curl gnupg2 software-properties-common

RUN curl -fsSL https://download.docker.com/linux/debian/gpg | apt-key add -

RUN add-apt-repository \
  "deb [arch=amd64] https://download.docker.com/linux/debian \
  $(lsb_release -cs) \
  stable"
 
RUN apt-get update -qq \
    && apt-get install docker-ce -y

RUN jenkins-plugin-cli --plugins docker-compose-build-step:1.0
RUN jenkins-plugin-cli --plugins docker-workflow:1.28
RUN jenkins-plugin-cli --plugins python:1.3

RUN usermod -aG docker jenkins