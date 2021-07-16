# README

This is an Ansible pull based setup. With no control node

## Subscribe a new host

1. Create a new file for the node named _{new_node_hostname}.yml_.

   ```yaml
   ---
   - name: Playbook for the {new_node_hostname} node
     hosts: {new_node_hostname}

     roles:
       - common
   ```

2. Install Ansible on the node
3. Run;  
   `ansible-pull -d /etc/ansible/ansible-cm --checkout master -U https://github.com/soofstad/ansible-cm -i "$(hostname)," "$(hostname).yml"`

Done!  
The host will now pull and apply playbooks from this repo every hour
