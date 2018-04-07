# Provisioning SakuraVPS by Ansible

CentOS7

test ansible connection

    % ansible xxx.xxx.xxx.xxx -m ping -c ssh -k

init

    % ansible-playbook init.yml -k

setup

    % ansible-playbook setup.yml --ask-become-pass -i "xxx.xxx.xxx.xxx:xxxx," --user=oppara 

setup (dry-run)

    % ansible-playbook setup.yml -C --ask-become-pass -i "xxx.xxx.xxx.xxx:xxxx," --user=oppara 

## Vagrant

    % cd /path/to/Vagrantfile-dir
    % vagrant ssh-config --host foo >> ~/.ssh/config

    % cd /path/to/setup.yml-dir
    % ansible -i "foo," foo -m ping 
    % ansible-playbook -i "foo," setup.yml --extra-vars "mysql_user_password=PassW0rd"
