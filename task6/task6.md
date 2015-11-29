# Task6:

Using ansible cloud modules gives you easy ways to automate deployments on enviroments like Amazon AWS.

In this task you'll first manage a cloud environment through an static inventory and later using a dynamic inventory.

1. Using the static inventory you should be able to setup the base servers.

2. Using dynamic inventory you should be able to run a deployment in which you should give an extra variable. As a result this variable will be used to replace the key on index.html file.

i.e.

ansible-playbook deploy.yml --extra-vars "event_name=prueba"

As a result it will set up a website with the message:

Hello prueba attendants!

Servers are behind an Amazon AWS ELB. The playbook will one by one get the server out of the load balancer, perform the deploy and bring the server back to the balancer.
