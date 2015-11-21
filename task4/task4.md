# Task4:

Roles are ways of automatically loading certain vars_files, tasks, and handlers based on a known file structure. Grouping content by roles also allows easy sharing of roles with other users.(*)

In this task you'll have an enviroment of a frontend webservers and a database server (we'll ignore thingse related to load balancers). Our stack is this:

Frontend webservers:
- git
- htop
- vim
- tomcat (port 8080)
- nginx (port 80 proxy passing to 8080)

Database server:
- git
- htop
- vim
- mysql-server (root password: cocotero)

Even if task4.yml seems a simple playbook it does a lot of things. It uses roles, some written by us and some others taken from [Ansible galaxy] (https://galaxy.ansible.com).

"common" and "nginx" are written by us the same way as previously we executed some tasks to all hosts now we include the role in those servers which require it.

(*) Taken from ansibles documentation
