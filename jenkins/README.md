
####   Note

1. JAVA_HOME  1.8 at  /usr/lib/jvm/java-8-openjdk-amd64
2. MAVEN at  /usr/share/maven

### To build
`` 
 docker build -t hcp/jenkins .
``
### To Run
``
docker run  -v /var/jenkins:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock -v $(which docker):/bin/docker -p 8080:8080 -p 50000:50000 -d hcp/jenkins
``

or add --privileged
using volume container
``
docker run --name hcp/jenkins -p 8080:8080 -p 50000:50000 -v /var/jenkins_home  hcp/jenkins
``

To access terminal
``
docker run -v /var/run/docker.sock:/var/run/docker.sock -v $(which docker):/bin/docker -i -t hcp/jenkins  /bin/bash  
``

Docker Host Default: tcp://172.17.0.1:2375

http://blog.yohanliyanage.com/2015/05/docker-clean-up-after-yourself/