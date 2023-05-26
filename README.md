Linux server: Ubuntu Server 22.04.2 LTS
ISO link: https://ubuntu.com/download/server

The user used is called "vboxuser". This is relevant as it's used in both the directory to create the file for the first task as well as to set it as the file owner in another.

To run the playbook, enter the machine, change the directory (cd) to where the playbook is on the machine and run the following command:
ansible-playbook appsilon.yml

Keep in mind this was developed in the following directory, which is once more relevant as that's also the directory used to create and copy files: /home/vboxuser/ansible-playbooks

______________________________

Task: Configure a Linux machine with Ansible

Note: You can use a different Configuration Management tool (such as Puppet or Chef), if you don’t feel comfortable with Ansible. But remember that we mostly use Ansible (and Terraform) at Appsilon.

To Do:
1) Prepare a machine with your favorite Linux (server) distribution. It can be a virtual machine set up with your local hypervisor, an EC2 instance at AWS, or a container run locally. It's up to you. Provide information what have you chosen, and how you prepared the machine (in a README):

● Information about the distribution (name, version, ISO/AMI link)

● If you provisioned the EC2 instance, shortly describe how you did that. If you use
Terraform, please provide the code. If you worked with AWS Web Console, tell us
what size of instance you used, which AMI, etc.

● If you used a container, provide the image name/Dockerfile, and instructions how
to run it

● If you use any other method, describe it

2) Create a playbook which do the following:

	2.1) Each new user should have a script called nice-script.sh in their home directory (hint: use "skeleton directory"). The script should list all mounted filesystems.
	
		2.1.1) Create the script with the correct command (locally)
		
		4.1.2) Copy the script to the remote machine into the correct directory
		
	2.2) Creates a user with:
	
		2.2.1) Username: john
		
		4.2.2) Home: /better-place/john (create /better-place before if needed)
		
		4.2.3) User ID: 1234
		
	2.3) User john should be able to run the following command with sudo without a need to provide his password: whoami
	
	4.4) Install packages:
	
		2.4.1) Tmux
		
		4.4.2) vim
		
	2.5) Install Terraform CLI (documentation)
	
3) Shortly describe how to run the playbook in README
