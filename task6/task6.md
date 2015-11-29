# Task6:

Using ansible cloud modules gives you easy ways to automate deployments on enviroments like Amazon AWS.

In this task you'll first manage a cloud environment through an static inventory and later using a dynamic inventory.

Servers are behind an Amazon AWS ELB. The playbook will one by one get the server out of the load balancer, perform the deploy and bring the server back to the balancer.

