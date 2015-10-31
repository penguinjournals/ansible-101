# Task3:

Playbooks are Ansible’s configuration, deployment, and orchestration language. They can describe a policy you want your remote systems to enforce, or a set of steps in a general IT process.
If Ansible modules are the tools in your workshop, playbooks are your design plans. (*)

In this task you'll have an enviroment of two frontend webservers and a database server (we'll ignore things related to load balancers). Our stack is this:

Frontend webservers:
- git
- memcached
- apache2
- libapache2-mod-php5

Database server:
- git
- mysql-server

We'll use apache with its default configuration and you'll have to remove original index.html and replace it with the index.php file in the folder.

If the task finishes correctly you should be able to see a web server in 10.0.0.2 and 10.0.0.3.

# Task3:(bis)

Memcached wasn't what we were looking for. Instead we've choose to install redis-server on database server. Which is your approach for facing it?
