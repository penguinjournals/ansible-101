# Task2:

Inventory file is the key when you want to manage multiple hosts at once. Here you have a 3 machine inventory defined on your vagrant file. You have a host.initial file with the IP of your virtual machines.

1. Start your vagrant environment defined in this folder

    vagrant up

2. Acording to your ansible.cfg create a hosts file based on the data in hosts.initial. The file has to match those rules:
    * You have to be able to call each machine by it's name instead of it's IP (frontend IP 10.0.0.2,backend IP 10.0.0.3, database IP 10.0.0.4)
    * You have to be able to call both application server at once.
    * You are encouraged to keep in mind that you may have serveral frontend, backend or databases in the future (groups, groups everywhere). 

    Look at hosts.answer file. You will notice groups created for frontends,backends and databases, even if not needed it's a good idea to be prepared for the future. Isn't your project the next billion idea? Pay special attention at the concept of group of groups defined as [application:children]
  
3. You've been noticed about the DROWN Bug and you need to update openssl package in all of them.

    ansible all -m command -a 'apt-get update && apt-get install -y openssl' --become
    ansible all -m apt -a 'update_cache=yes name=openssl state=latest' --become

4. Extra ball:
    * How would you create a user for each role of server (frontuser,backuser and databaseuser).

    You should include users name on group_vars/role.yml so that is used when running each host and with the user module run:
    ansible all -m user -a "name={{ user }}" -become

    As you can see, using modules gives you a better feedback of the execution and are a good way to idempotence as far as you describe states more than instructions. You can take a look to all available modules at:
    http://docs.ansible.com/ansible/modules_by_category.html

    There are also unofficial modules and you can write your owns. Ask Google ;)
