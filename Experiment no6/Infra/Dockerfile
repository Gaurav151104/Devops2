
FROM jenkins/jenkins:lts

USER root

RUN apt-get update && \
    apt-get install -y git tidy && \
    rm -rf /var/lib/apt/lists/*

USER jenkins
