Como Rodar? 
==========

https://docs.mv.com.br/display/infraestrutura/Chef-Server+Ansible+Playbook


### Com private_key:

- ansible-playbook -b playbook.yml 

### Com senha:

- ansible-playbook -b -K playbook.yml

### Passando agent version 

- ansible-playbook -b -K playbook.yml --extra-vars "gcm_version=$version" 

Se não passar a gcm_version, ele baixa automaticamente a versão 1.5.3.


### NEW! 

 Instalação de novos agentes, seguir documentação: 

 https://docs.mv.com.br/display/infraestrutura/Ansible+%7C+Criar+Executores+Portal




