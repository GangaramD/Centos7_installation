
# Jenkins on centos:

Java on Centos RHEL7:

	  $ sudo yum install java-1.8.0-openjdk-devel

	  $ java -version

	  $ sudo yum remove java-1.8.0-openjdk-devel

 Jenkins:
	   
	   $ curl --silent --location http://pkg.jenkins-ci.org/redhat-stable/jenkins.repo | sudo tee /etc/yum.repos.d/jenkins.repo
	  
	      $ sudo rpm --import https://jenkins-ci.org/redhat/jenkins-ci.org.key
	  
	            And add the repository to your system with:

	      $ sudo rpm --import https://jenkins-ci.org/redhat/jenkins-ci.org.key

	      $ sudo yum install jenkins

	      $ sudo systemctl start jenkins

	      $ systemctl status jenkins

 




