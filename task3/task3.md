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
- redis-server

We'll use apache with its default configuration and you'll have to remove original index.html and replace it with the index.php file in the folder. Tip: index.html is placed into /var/www/html and there has index.php to be placed too.

If the task finishes correctly you should be able to see a web server in 10.0.0.2 and 10.0.0.3.

# Task3, steps:

1. Run task3-first-step.yml playbook. You'll get git installed in all your machines. You limit the scope of execution with the hosts parameter and use the apt module to install git. Re-run task3-first-step.yml to see an example of idempotence.

2. Fill the task3-second-step.yml playbook so that you achieved what is required. 

3. Run task3-second-step.yml and hit 10.0.0.2 or 10.0.0.3 to see your web servers up and running.

4. Edit index.php file and re-run task3-second-step.yml, notice the state change on the execution log to see which of the tasks have changed their state. Open your browser to see your change applied.

(*) Taken from ansibles documentation
