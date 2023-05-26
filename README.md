Linux server: Ubuntu Server 22.04.2 LTS
ISO link: https://ubuntu.com/download/server

The user used is called "vboxuser". This is relevant as it's used in both the directory to create the file for the first task as well as to set it as the file owner in another.

To run the playbook, enter the machine, change the directory (cd) to where the playbook is on the machine and run the following command:
ansible-playbook appsilon.yml

Keep in mind this was developed in the following directory, which is once more relevant as that's also the directory used to create and copy files: /home/vboxuser/ansible-playbooks
