# ansible_practice

This is my awesome Ansible repository


commands:

alias ssha='eval $(ssh-agent) && ssh-add'

ssha

passphrase: ansible training


ansible all --key-file ~/.ssh/ansible - i inventory

ansible all --key-file ~/.ssh/ansible -i inventory -m ping


"make ansible.cfg file for inventory & private key"

ansible all -m ping

ansible all --list-hosts

ansible all -m gather_facts

ansible all -m gather_facts --limit 192.168.18.213


"sudo previliges: "
ansible all -m apt -a update_cache=true
ansible all -m apt -a update_cache=true --become --ask-become-pass
or "sudo apt update"

ansible all -m apt -a name=vim-nox --become --ask-become-pass

check on server
which vim
apt search vim-nox

ansible all -m apt -a name=tmux --become --ask-become-pass

ansible all -m apt -a name=snapd --become --ask-become-pass

ansible all -m apt -a "name=snapd state = latest" --become --ask-become-pass

ansible all -m apt -a "upgrade=dist" --become --ask-become-pass
or sudo apt dist-upgrade



ansible-playbook --ask-become-pass install_apache.yml

inventory2 (CentOS):
172.16.250.248 apache_package=httpd php_package=php
