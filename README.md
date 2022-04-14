# Jenkins-SCM

Jenkins build and publish images on Docker Hub.

## Installation

**Prerequisites:**
- Docker >= 19.03.13

To install Docker Engine follow steps given in [Install Docker Engine](https://docs.docker.com/engine/install/).

- Docker Compose
[Install Docker Compose]( ).

## Usage

1. Clone the project locally

```
git clone https://github.com/VictorGil-sys/Jenkins-SCM.git
```

2. Run a docker-compose

```
docker-compose -f ./Jenkins-Container/docker-compose.yaml up -d
```

3. Runnning application

```
http://127.0.0.1:8080
```

Use the initial password, show in '/var/jenkins_home/secrets/initialAdminPassword' or show it in container logs:

```
docker exec jenkins-container cat /var/jenkins_home/secrets/initialAdminPassword
```

![](https://github.com/VictorGil-sys/Jenkins-SCM/blob/main/images/2-Started_credentials.png)


![](https://github.com/VictorGil-sys/Jenkins-SCM/blob/main/images/1-Jenkins_started.png)

4. Install Plugins

Install Suggested Plugins and later, from Plugin Manager:
```
- Docker Pipeline
- Git Plugin
- Docker Compose Build Step
```

# CREATE a Jobs

1. Create credentials for Docker Hub and Github repo

![](https://github.com/VictorGil-sys/Jenkins-SCM/blob/main/images/3-Credentials.png)

2. Create Pipeline

![](https://github.com/VictorGil-sys/Jenkins-SCM/blob/main/images/4-Create_pipeline.png)

3. Configure pipeline

![](https://github.com/VictorGil-sys/Jenkins-SCM/blob/main/images/5-Configure_pipeline1.png)

![](https://github.com/VictorGil-sys/Jenkins-SCM/blob/main/images/6-Configure_pipeline2.png)

4. Configure SCM
#TODO
