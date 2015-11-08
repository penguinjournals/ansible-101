# Task4:

Roles are ways of automatically loading certain vars_files, tasks, and handlers based on a known file structure. Grouping content by roles also allows easy sharing of roles with other users.(*)

In this task you'll have an enviroment of a frontend webservers and a database server (we'll ignore thingse related to load balancers). Our stack is this:

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

# Task3:(bis)

Memcached wasn't what we were looking for. Instead we've choose to install redis-server on database server. Which is your approach for facing it?

(*) Taken from ansibles documentation
