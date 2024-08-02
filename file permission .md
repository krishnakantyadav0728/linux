### How to chanage default file permission 

	#umask

permission will be .

permission = 0777 - 0022 = 	0755

	#umask -S
	
	#umask u+rw,g+rw,o-r
	
To change default permission permanently.

Add the permission in .bashrc file.

To change globally.

#less /etc/bashrc

#vi .bashrc

umask o-r

:wq

#source .bashrc -> for load the permission

