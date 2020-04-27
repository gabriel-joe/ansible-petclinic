### Run for debian:

- ansible-playbook playbook-debian.yml 

### Run for rhel:

- ansible-playbook playbook-rhel.yml

### Jenkins configuration

- ansible-playbook playbook-jenkins-configuration --extra-vars="url_jenkins=${URL}"
  - URL = Your IP and PORT that jenkins is running

URL = Your jenkins url

### Playbook (debian/rhel) will install/configurate

- Docker
- Build jenkins container with initial configuration
- Create dir to bind volume (/var/jenkins_home) in /home/jenkins_home
- Run Jenkins container
- User and password to access jenkins - admin/admin

### Playbook (Jenkins configuration) will configurate

- Job setup to be ready to build





