Super quick playbook to install puppet 5 on a windows server. 

To create vault file with required credentials to run this on a windows host: 
ansible-vault create external_vars.yml

Contents should contain: 
ansible_user: userhere
ansible_password: passwdhere

host file in exampe below should contain the fqdn or ip for the target server:
[target]
192.168.1.123
host.zype76.com 

To execute: 
ansible-playbook windowsbuild.yml -i host
