# Ansible 

Is a powerful automation tool that simplifies the management of IT infrastructure. Setting up Ansible on a Linux Server is the first step towards leveraging its capabilities. This will guide you through installing and configuring Ansible on a linux server, allowing ofr the automation of tasks and to manage servers effectively.

## Task 1

### Install Ansible on Controller


For configuration of Ansible and target/worker machine, terraform was used to set it entirely up. User-data scripts were used to install Anisble on the controller and python the worker. 
NB: To make sure python3 is installed on the worker.

The images below so the terraform structure alongside plan & apply commands applied

![](img/a.creating-resources.png)
![](img/b.vpc-setup.png)
Next: The instances created and placed side by side.
![](img/c.instances-creation.png)
![](img/c.instances.png)

### Configure SSH into target:worker
First, in the controller machine, a command is run to confirm the successful installation.
![](img/d.check-ansible-on-host.png)

### Create inventory file for targert:worker

![](img/d.inventoryfile.png)

### Test Ansible connectivity
ssh is configured using the worker ip address added to the inventory file and the keypair

![](img/f.pingworker.png)
![](img/e.sshintoworker.png)


### Run simple AdHoc commands
Simple commands to;

Check Uptime:
![](img/g.checkworkeruptime.png)

Check disk space:
![](img/h.checkdiskspace.png)


Additionally, manually monitoring was incorperated:
![](img/i.monitoring.png)




## Task 2

Managing user accounts is a common admin task for linux servers. Manually creating and managing user accounts, that have access to the servers. Ansible simplifies the process by automating user creation with playbooks.


### Create an ansible playbook to automate user creation

![](img/j.createusers.png)

### Run the playbook using the ansible comamand

This creates the users, script uses the latest syntax 

![](img/k.run-pb.png)

show cofirmation 

![](img/l.creating.png)

To show confirmation ssh into worker/target machine and run command

![](img/m.ssh_n_confirm.png)

### Add group and ssh key configuration & then show confirmation

![](img/n.ssh_users.png)

![](img/o.script.png)

![](img/p.creating.png)

![](img/q.confirm.png)

![](img/r.confirm.png)
 