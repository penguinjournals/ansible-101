# Task1:

Ansible is agentless, the only thing you need to start trying Ansible is Ansible, and SSH access to the hosts you want to manage.

In this task, you have to achieve the next goals:
-Start your vagrant machine defined in this folder
vagrant up

-Check that you can access the machine with Ansible
ansible all -m ping

-Check the date and time of the machine
ansible task1 -a 'date'

-Get a list of the files in /root folder
ansible task1 -a 'ls /root' --sudo
