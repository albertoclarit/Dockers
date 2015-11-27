FROM jenkins
# if we want to install via apt
USER root
RUN apt-get update && apt-get install -y maven && apt-get install -y docker-engine && usermod -g docker
VOLUME /var/run/docker.sock
# drop back to the regular jenkins user - good practice
USER jenkins
