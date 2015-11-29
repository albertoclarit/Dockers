
####   Note

1. JAVA_HOME  1.8 at  /usr/lib/jvm/java-8-openjdk-amd64
2. MAVEN at  /usr/share/maven

### To build
`` 
 docker build -t hcp/jenkins .
``
### To Run
``
docker run  -v /var/jenkins:/var/jenkins_home  -p 8080:8080 -p 50000:50000 -d hcp/jenkins
``

### Or You can create and start
``
docker create  -v /var/jenkins:/var/jenkins_home  -p 8080:8080 -p 50000:50000 -d -name=hcp_jenkins  hcp/jenkins
docker start hcp_jenkins
``
 if name is not specified, docker will give a random name
or add --privileged
using volume container
``
docker run --name hcpjenkins -p 8080:8080 -p 50000:50000 -v /var/jenkins_home -d hcp/jenkins
``

To access terminal
``
docker run  -i -t hcp/jenkins  /bin/bash  
``

Docker Host Default: tcp://172.17.0.1:2375

http://blog.yohanliyanage.com/2015/05/docker-clean-up-after-yourself/