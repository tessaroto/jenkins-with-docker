Jenkins with docker installed


Cloning the projeto
```
git clone https://github.com/tessaroto/jenkins-with-docker.git
cd jenkins-with-docker
```

Building image
```
$ docker build -t jenkins-with-docker .
```

Running
```docker run \
  -p 8080:8080 \
  -v /walmart/temp/volume/jenkins_home:/var/jenkins_home \
  -v /var/run/docker.sock:/var/run/docker.sock \
  --name jenkins \
  jenkins-with-docker ```

