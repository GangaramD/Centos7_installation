
# Jenkins on centos:

  	    $ curl --silent --location http://pkg.jenkins-ci.org/redhat-stable/jenkins.repo | sudo tee /etc/yum.repos.d/jenkins.repo
	  
	      $ sudo rpm --import https://jenkins-ci.org/redhat/jenkins-ci.org.key
	  
	            And add the repository to your system with:

	      $ sudo rpm --import https://jenkins-ci.org/redhat/jenkins-ci.org.key

	      $ sudo yum install jenkins

	      $ sudo systemctl start jenkins

	      $ systemctl status jenkins

 



