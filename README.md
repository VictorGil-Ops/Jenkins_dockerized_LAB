# Jenkins-SCM

Jenkins build and publish images in Docker Hub.

## Installation

**Prerequisites:**
- Docker >= 19.03.13

To install Docker Engine follow steps given in [Install Docker Engine](https://docs.docker.com/engine/install/).

## Usage

1. Clone the project locally

```
git clone https://github.com/VictorGil-sys/Jenkins-SCM.git
```

2. Run a docker-compose

```
docker-compose up -d
```

3. Runnning application

```
http://127.0.0.1:8080
```

Use the initial password, show in '/var/jenkins_home/secrets/initialAdminPassword' or on container logs:

```
docker logs jenkins-container
```
![](https://github.com/VictorGil-sys/Jenkins-SCM/blob/main/images/2-Started_credentials.png)


![](https://github.com/VictorGil-sys/Jenkins-SCM/blob/main/images/1-Jenkins_started.png)

4. Install Plugins

Install Suggested Plugins and later, from Plugin Manager:
```
- Docker Pipeline
- Git Plugin
```

# CREATE a Jobs

1. Create credentials for Docker 

![](https://github.com/VictorGil-sys/Jenkins-SCM/blob/main/images/2-Credentials.png)