## Jenkins with docker installed

### Cloning the projeto
```
git clone https://github.com/tessaroto/jenkins-with-docker.git
cd jenkins-with-docker
```

### Building image
```
$ docker build -t jenkins-with-docker .
```
### Running
Create a directory and configure the docker to allow this directory use as volume.
/temp/volume/jenkins_home
Or change to a path to a directory that has the necessary permission. 
``` 
$ docker run \
  -p 8080:8080 \
  -v /temp/volume/jenkins_home:/var/jenkins_home \
  -v /var/run/docker.sock:/var/run/docker.sock \
  --name jenkins \
  jenkins-with-docker 
```

### Open Jenkins 
``` 
$ open http://localhost:8080
```
