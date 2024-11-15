# About
Here there is an attempt to create a Vagrant VM and install kubernetes kubeadm with Ansible.

# Setup
```/shell
mkdir ssh_keys
```
```/shell
ssh-keygen -t rsa -b 4096 -C "ansible@localhost" -f ./ssh_keys/id_rsa
```

# Commands
```/shell
vagrant up
```
```/shell
ansible-playbook playbook.yml
```
