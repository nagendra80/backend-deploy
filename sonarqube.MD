## SonarQube SetUp

* Login to bastion host and Setup Sonar Qube
```
sudo dnf -y install dnf-plugins-core
```

```
sudo dnf config-manager --add-repo https://download.docker.com/linux/rhel/docker-ce.repo
```

```
sudo dnf install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin -y
```

```
sudo systemctl start docker
```

```
sudo systemctl enable docker
```

```
sudo usermod -aG docker ec2-user
```

```
docker images
```
* Use this sonarqube:lts-community which i will get it from docker hub
```
docker run -d --name sonarqube -p 9000:9000 sonarqube:lts-community
```

* check the docker running images
```
docker ps
```
