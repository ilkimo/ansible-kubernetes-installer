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
## Launch Vagrant
To launch vagrant, enter in a directory that contains a ``Vagrantfile``, then launch:
```/shell
vagrant up
```

## Launch Ansible provisioning
```/shell
ansible-playbook playbook.yml
```
