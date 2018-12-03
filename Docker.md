# Installing Docker on CentOS7

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


