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






 



