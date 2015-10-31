# Task2:

Inventory file is the key when you want to manage multiple hosts at once. Here you have a 3 machine inventory defined on your vagrant file. You have a host.initial file with the IP of your virtual machines.

In this task, you have to achieve the next goals:
-Start your vagrant environment defined in this folder

vagrant up

-Acording to your ansible.cfg create a hosts file based on the data in hosts.initial. The file has to match those rules:
..-You have to be able to call each machine by it's name instead of it's IP.
...-frontend IP 10.0.0.2
...-backend IP 10.0.0.3
...-database IP 10.0.0.4
..-You have to be able to call both application server at once.
..-You are encouraged to keep in mind that you may have serveral frontend, backend or databases in the future (groups, groups everywhere).

Look at hosts.answer file. You will notice groups created for frontends,backends and databases, even if not needed it's a good idea to be prepared for the future. Isn't your project the next billion idea? Pay special attention at the concept of group of groups defined as [application:children]

-You've been noticed about the Heartbleed Bug and you need to update openssl package in all of them.

ansible all -a 'apt-get install -y openssl' --sudo
