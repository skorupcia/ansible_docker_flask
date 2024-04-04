# ansible_docker_flask
Ansible Flask app with Docker

## Specifications

macOS: Sonoma 14.2.1

Ubuntu: 20.04

Parallels: 19.3.0

## RUN INSTRUCTIONS

1. Install docker collection:

  ansible-galaxy collection install community.docker

2. Run required roles:

  ansible-galaxy install -r requirements.yml

3. Run vagrant in the directory:

  vagrant up

4. Setup etc/hosts file:

  192.168.56.39  docker-flask.test


## Links 

   https://github.com/geerlingguy/ansible-for-devops/tree/master/lamp-infrastructure

   2nd edition of Ansible for DevOps Jeff Geerling