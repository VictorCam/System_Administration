# Running Ansible with a Webserver (docker)

System Administration Homework 3

## Description

In each file we have the neccesary components to run the webserver and ansible playbook.

## How to run

docker run -p 22 -it --rm --name u1 --network CS312LAN victorcampa/f_controller:latest

docker run -p 22 -it --rm --name u2 --network CS312LAN victorcampa/f_node:latest

[ON u1 = CONTROLLER] change the ip on hosts.ini to the name you apply to the node (in this case u2)

[ON u2 = NODE] run the command "service sshd restart"

[ON u1 = CONTROLLER] run "ansible mynodes -i ~/hosts.ini -m ping" which SHOULD ping back

[ON u1 = CONTROLLER] "ansible-playbook ~/webserver.yaml -i ~/hosts.ini" (note I modified the playbook in order to get apache2 working on docker)

[on u1 = CONTROLLER] run "curl u2" or whatever name you gave to the container
