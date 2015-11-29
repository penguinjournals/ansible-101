# Task2:

Inventory file is the key when you want to manage multiple hosts at once. Here you have a 3 machine inventory defined on your vagrant file. You have a host.initial file with the IP of your virtual machines.

1. Start your vagrant environment defined in this folder
2. Acording to your ansible.cfg create a hosts file based on the data in hosts.initial. The file has to match those rules:
    * You have to be able to call each machine by it's name instead of it's IP (frontend1 IP 10.0.0.2,backend1 IP 10.0.0.3, database1 IP 10.0.0.4)
    * You have to be able to call both application server at once.
    * You are encouraged to keep in mind that you may have serveral frontend, backend or databases in the future (groups, groups everywhere). 
3. You've been noticed about the Heartbleed Bug and you need to update openssl package in all of them.

[Tip] (http://docs.ansible.com/ansible/intro_inventory.html)
