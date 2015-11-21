# Task5:

Ansible allows you to deploy and configure using the same tool, so you would likely reuse groups and just keep the OS configuration in separate playbooks from the app deployment.(*)

In this task you'll deploy a really simple webapp:

First you should run the setup.yml playbook. It will setup a server with apache running.

1. Download locally a copy of the git repo in the required version to get the configuration template file

2. Clean remotes temporary folder

3. Download required version to destination servers temporary folder

4. Rewrite configuration file

5. Deploy remotely the new version of the software

(*) Taken from ansibles documentation
