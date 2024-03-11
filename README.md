# ansible

Ansible is a suite of software tools that enables infrastructure as code. It is open-source and the suite includes software provisioning, configuration management, and application deployment functionality.

Ansible is a software tool that provides simple but powerful automation for cross-platform computer support. It is primarily intended for IT professionals, who use it for application deployment, updates on workstations and servers, cloud provisioning, configuration management, intra-service orchestration, and nearly anything a systems administrator does on a weekly or daily basis.

![image](https://github.com/TauqeerAhmad5201/ansible/assets/68806440/95bfce1e-f21c-4e7a-b458-1e5f9de4a321)

DOCS: https://docs.ansible.com/

Ansible Module: https://docs.ansible.com/ansible/2.9/modules/list_of_all_modules.html

## inventory-file
hosts   
/home/ubuntu/ansible/hosts (can be defined anywhere) 

## checking the inventory which contains all the hosts and servers with IP 

```
ansible-inventory --list -y -i /home/ubuntu/ansible/hosts
```
##  ping to all the connected nodes

```
ansible all -m ping -i /home/ubuntu/ansible/hosts --private-key=/home/ubuntu/.ssh/ansible_key
```
## running the ansible playbook 
```
anisble-playbook <playbook_name.yml> -i /home/ubuntu/ansible/hosts --private-key=/home/ubuntu/.ssh/ansible_key
```
## ad hoc command - where linux command is used
```
ansible all (groups) -a "sudo apt install nginx" -i /home/ubuntu/ansible/hosts --private-key=/home/ubuntu/.ssh/ansible_key
```
```
ansible demo -ba "apt remove nginx -y" 
```

## ansible module command - oneliner 
```
ansible servers -b -m apt -a "pkg=git state=present"
```

## commands to use 

https://www.javatpoint.com/ansible-command 
https://www.javatpoint.com/ansible
