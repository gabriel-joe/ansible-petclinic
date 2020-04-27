### Run for debian:

- ansible-playbook playbook-debian.yml 

### Run for rhel:

- ansible-playbook playbook-rhel.yml

### Jenkins configuration

- ansible-playbook playbook-jenkins-configuration --extra-vars="url_jenkins=${URL}"
  - URL = Your host that jenkins is running
  - Obs: assume the entire url including http:// or https://
  - eg: http://localhost:8080


### Playbook (debian/rhel) will install/configurate

- Docker
- Build jenkins container with initial configuration
- Create dir to bind volume (/var/jenkins_home) in /home/jenkins_home
- Run Jenkins container
- User and password to access jenkins - admin/admin

### Playbook (Jenkins configuration) will configurate

- Job setup to be ready to build





