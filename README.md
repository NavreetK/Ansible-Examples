# Ansible

Ansible is an open-source automation tool that is used for configuration management, application deployment, task automation, and IT orchestration. It simplifies complex infrastructure tasks and can be used to manage systems, deploy software, and automate various IT processes.
* It operates in an agentless manner, meaning that it doesn't require any software or agent to be installed on the target systems. It communicates with remote machines over SSH (for Linux/Unix systems) or WinRM (for Windows systems) to execute tasks.
* Ansible playbooks are written in YAML and contain a set of instructions (tasks) to be executed on remote systems. Playbooks describe a series of steps and define the desired state of the system.

We are using Ansible to install Apache2, nginx and MySQL on 2 different EC2 instances, OS of all of my instances including Master are Ubuntu OS.

# Prerequisistes
In order to be able to make deployments to the web servers, you must have a SSH connection to your machines from the master server, where you will run Ansible commands.

# Add Worker IPs in HostFile
Once you have achieved the SSH connections to your machines. You must add the IP addresses of worker nodes into the ansible-HostsFile which is created automatically while installing Ansible. 
Default location of ansible-hostfile - etc/ansible/hosts

I have grouped both IPs together and named the group as "Servers"

Once you have written your playbook.yml file you can execute it by using the following command:

```bash
ansible-playbook playbookname.yml
```
