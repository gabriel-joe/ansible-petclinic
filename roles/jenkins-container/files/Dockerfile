FROM jenkinsci/blueocean
#FROM jenkins 
USER root 
RUN addgroup -S jenkins docker && apk add sudo 
# install jenkins plugins
RUN /usr/local/bin/install-plugins.sh configuration-as-code configuration-as-code-support git mstest matrix-auth workflow-aggregator docker-workflow blueocean credentials-binding ldap maven-plugin
USER root
RUN apk update && apk add maven && apk add libxml2-utils
USER jenkins
ENV JENKINS_USER admin
ENV JENKINS_PASS admin

# allows to skip Jenkins setup wizard
ENV JAVA_OPTS -Djenkins.install.runSetupWizard=false

# Jenkins runs all grovy files from init.groovy.d dir
# use this for creating default admin user
COPY ./default-user.groovy /usr/share/jenkins/ref/init.groovy.d/

# volume for Jenkins settings
VOLUME /var/jenkins_home
VOLUME /var/run/docker.sock
