FROM jenkins
# if we want to install via apt
USER root
RUN apt-get update && apt-get install -y maven && apt-get install -y docker.io && usermod -aG docker jenkins
ENV DOCKER_HOST=tcp://172.17.0.1:2375
# drop back to the regular jenkins user - good practice
USER jenkins
