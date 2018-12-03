Adding a User in the Centos7 and give it a Sudo previlage:

		        $ adduser username

	Use the passwd command to update the new user's password.

				$ passwd username  

	Set and confirm the new user's password at the prompt. A strong
		           password is highly recommended!

				Set password prompts:
				Changing password for user username.
				New password:
				Retype new password:
				passwd: all authentication tokens updated successfully.      

	Use the usermod command to add the user to the wheel group.

				$ usermod -aG wheel username

	By default, on CentOS, members of the wheel group have sudo
		      privileges.


	Use the su command to switch to the new user account.

				$ su - username

	As the new user, verify that you can use sudo by prepending "sudo" to the command that you want to run with superuser privileges.

				$ sudo command_to_run

	For example, you can list the contents of the /root directory, which is normally only accessible to the root user.

				$ sudo ls -la /root

	The first time you use sudo in a session, you will be prompted for the password of the user account. Enter the password to proceed.

					Output:
					[sudo] password for username:
					If your user is in the proper group and you entered the password correctly, the command that you issued with sudo should run with root privileges.


Java on Centos RHEL7:

	  $ sudo yum install java-1.8.0-openjdk-devel

	  $ java -version

	  $ sudo yum remove java-1.8.0-openjdk-devel


Jenkins on centos:
	  $ curl --silent --location http://pkg.jenkins-ci.org/redhat-stable/jenkins.repo | sudo tee /etc/yum.repos.d/jenkins.repo
	  
	  $ sudo rpm --import https://jenkins-ci.org/redhat/jenkins-ci.org.key
	  
	      And add the repository to your system with:

	  $ sudo rpm --import https://jenkins-ci.org/redhat/jenkins-ci.org.key

	  $ sudo yum install jenkins

	  $ sudo systemctl start jenkins

	  $ systemctl status jenkins

 
Ansible:
	   To get Ansible for CentOS 7, first ensure that the CentOS 7 EPEL repository is installed:
	     	
	     	refrence: https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-ansible-on-centos-7 

	   	$ sudo yum install epel-release
	   	$ sudo yum install ansible


Installing terraform on CentOS7:

	 	$ sudo yum install -y zip unzip
	 	
	 	$ sudo apt-get -y install / sudo yum install -y zip unzip (if these are not installed)
	    
	    $ wget https://releases.hashicorp.com/terraform/0.9.8/terraform_0.9.8_linux_amd64.zip
	    
	    $ unzip terraform_0.9.8_linux_amd64.zip
	    
	    $ sudo mv terraform /usr/local/bin/

  Confirm terraform binary is accessible: 
  		$ terraform --version

Installing Docker on CentOS7

	Start by updating your system packages and install the required dependencies:

			$ sudo yum update
			$ sudo yum install yum-utils device-mapper-persistent-data lvm2
			
	Next, run the following command which will add the Docker stable repository to your system:

			$ sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
			
	Now that the Docker repository is enabled, install the latest version of Docker CE (Community Edition) using yum by typing:

			$ sudo yum install docker-ce
		
	Once the Docker package is installed, start the Docker daemon and enable it to automatically start at boot time:

			$ sudo systemctl start docker
			$ sudo systemctl enable docker

		
	To verify that the Docker service is running type:

			$ sudo systemctl status docker


