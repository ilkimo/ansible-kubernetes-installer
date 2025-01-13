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
### Cgroups v2 workaround
After initializing the Vagrant VM the first time, it is necessary to reboot it in order to apply the grub update done during provisioning (te enable cgroups v2 for kubernetes):
```/shell
vagrant ssh
```
```/shell
sudo reboot
```
A solution could be to use the reload plugin in the Vagrantfile, but I am having some dependency issues when installing the Vagrant reload plugin with ``vagrant plugin install vagrant-reload``

## Launch Ansible provisioning
```/shell
ansible-playbook playbook.yml
```
