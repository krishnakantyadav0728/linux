# Topic.
*how to swith a user

*how to exit of current user

*what is the use of sudo

*how to provide a sudo access to a user

*what is the visudo

*working with sudoers file

### how to change a user

#whoami---check

#su - username

su---switch user

### revert then do exit

#for root user

su -

### what is sudo

super user do.

it is a way to temporarily grant a user administrative rights.

ex:

#yum install nginx

#sudo yum install nginx

details of sudo is present under.

#/etc/sudoers

we can edit the above file using.

#visudo

#less /etc/sudoers

how to give limited access for any user.

#updatedb

#log as aroot user

#visudo

#allow  root to run commands

example

sunn  ALL=LOCATE 

