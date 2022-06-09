# Ansible Project
Ansible project to automatically join domain Active Directory using sssd for RedHat and Debian family OS.

# Requirements

- Ansible >= 2.7

# Steps

- Master step

If you want, there are details of the steps :
- Update systems
- Rename hostname (optional)
- Install required packages
- Join system to the domain

# How to run a playbook

- Modify inventory file :
Add your IP
```
yaml
[group_name]
0.0.0.0 (ansible_ssh_user=[default_account]) (new_hostname=[hostname])
yaml
```

Exemple :

```
yaml
192.168.1.1 ansible_ssh_user=rocky new_hostname=ROCKY001 
yaml
```

- Navigate to the project root
ansible-playbook tasks/[filename_step] test/inventory

# Testing

This project has been tested on these Linux distributions :

- Rocky Linux 8 / CentOS 8 / RHEL 8
- Debian 10
- Ubuntu 18.04
