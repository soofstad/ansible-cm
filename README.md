# README

This is an Ansible pull based setup. With no control node

## Subscribe new host

1. Install Ansible
2. Run;   
   `ansible-pull -d /etc/ansible/ansible-cm --checkout master -U https://github.com/soofstad/ansible-cm -i "$(hostname),"`

Done!  
The host will now pull and apply playbooks from this repo every hour
