FROM jenkins/jenkins:lts

USER root
RUN apt-get -qq update \
  && apt-get -qq -y install \
  curl

RUN curl -sSL https://get.docker.com/ | sh

RUN curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
RUN chmod +x /usr/local/bin/docker-compose

RUN echo "Asia/Shanghai" > /etc/timezone

RUN usermod -a -G staff jenkins

USER jenkins
