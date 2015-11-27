
####   Note

1. JAVA_HOME  1.8 at  /usr/lib/jvm/java-8-openjdk-amd64
2. MAVEN at  /usr/share/maven

### To build
`` 
 docker build -t hcp/jenkins .
``
### To Run
``
docker run -p 8080:8080 -p 50000:50000 -v /var/jenkins:/var/jenkins_home hcp/jenkins
``

using volume container
``
docker run --name hcp/jenkins -p 8080:8080 -p 50000:50000 -v /var/jenkins_home  hcp/jenkins
``

To access terminal
``
docker run -i -t hcp/jenkins /bin/bash  
``