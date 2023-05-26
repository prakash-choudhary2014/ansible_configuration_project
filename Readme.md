# Ansible Playbook Readme

This repository contains Ansible playbooks and inventory files for managing servers. The following commands and instructions will help you perform various tasks.

## Prerequisites
- Ansible should be installed on your local machine.
- Ensure you have SSH access to the target servers with the appropriate SSH key configured.

## Inventory
To list all servers in the inventory, run the following command:
```
ansible-inventory --list -y -i /home/ubuntu/ansible/hosts
```

## Ping All Servers
To ping all servers in the inventory, use the following command:
```
ansible all -m ping -i /home/ubuntu/ansible/hosts --private-key=~/.ssh/ansible_key
```

## Run create_file.yml Playbook
To execute the `create_file.yml` playbook and create files on the servers, run the following command:
```
ansible-playbook create_file.yml -i /home/ubuntu/ansible/hosts --private-key=~/.ssh/ansible_key
```

## Run createuser.yml Playbook
To run the `createuser.yml` playbook and create users on the servers, execute the following command:
```
ansible-playbook createuser.yml -i /home/ubuntu/ansible/hosts --private-key=~/.ssh/ansible_key
```

## Run docker.yml Playbook
To execute the `docker.yml` playbook and manage Docker containers on the servers, use the following command:
```
ansible-playbook docker.yml -i /home/ubuntu/ansible/hosts --private-key=~/.ssh/ansible_key
```

Please ensure that you modify the command parameters (e.g., inventory file path, SSH key path) according to your specific setup.

For any further information or assistance, feel free to contact the repository maintainers.

**Note:** Ensure that you review and understand the playbooks and their respective tasks before running them on production servers.