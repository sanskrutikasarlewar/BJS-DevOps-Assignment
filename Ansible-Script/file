#install docker sdk fro python
$ pip3.8 install docker

#Install Required Ansible-collection in your host to use Inventory plugin
$ ansible-galaxy collection install community.docker

#setup ansible config file
$ cat /etc/ansible/ansible.cfg
[defaults]
inventory      = /etc/ansible/hosts
roles_path    = /etc/ansible/roles
host_key_checking = False

#Setup Inventory Plugin for Docker:
$ cat /etc/ansible/hosts/main_docker.yml
plugin: community.docker.docker_containers
docker_host: unix://var/run/docker.sock

#Test the setup that it worked or not:
$ docker run -dit --name test centos:latest

#Now run command to check container using Ansible Plugin:
$ ansible-inventory --graph
