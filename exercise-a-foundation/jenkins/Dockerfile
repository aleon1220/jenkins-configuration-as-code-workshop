FROM docker.io/jenkins/jenkins:lts

LABEL maintainer="<leonard.sheng.sheng.lee@gmail.com> and aditions by www.andres.nz"

ARG JAVA_OPTS
ENV JAVA_OPTS "-Djenkins.install.runSetupWizard=false ${JAVA_OPTS:-}"

ENV JENKINS_HOME "/var/jenkins_home"

USER jenkins

COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN xargs /usr/local/bin/install-plugins.sh </usr/share/jenkins/ref/plugins.txt

COPY jenkins.yaml /usr/share/jenkins/ref/jenkins.yaml
