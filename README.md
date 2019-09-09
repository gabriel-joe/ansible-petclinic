### Run for debian:

- ansible-playbook playbook-debian.yml 

### Run for rhel:

- ansible-playbook playbook-redhat.yml

### Jenkins configuration

- ansible-playbook playbook-jenkins-configuration --extra-vars="url_jenkins=${URL}"

URL = Your jenkins url

### Playbooks will install

- docker
- run jenkins container
- User and password to access jenkins - admin/admin







