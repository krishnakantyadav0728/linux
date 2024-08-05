### SELinux 

what is SELinux.

security-Enhanced linux

- A linux kernel security module

- provides additional layer of access control and mandatory access control (MAC) to enhance the security


DAC VS MAC.



SELinux options (SELinux work on three mode)

- enforcing (by default enabled in redhat)

- permissive (disabled but logs the activity)

- disable

how to check SELinux status.

#sestatus or getenforce

change SELinux settings?.

#setenforce 0 = Permissive/Disable

#setenforce 1 = Enable

Change SELinux settings permanent.

#/etc/selinux/config

SELinux=enforcing/disable/permissive.

create a file before rebooting.

#fixfiles -F onboot

/.autorelable

To prevent incorrectly labeled and unlabeled files from causing problems SELinux automatically relables file
systems when changing from the disabled state to permissive or enforcing mode.

Before rebooting the system for relabeling  make sure the system will boot in permissive mode for example 
by using the enforcing=0 kernel options.

Two main concepts of SELinux 

- labeling 

- Type enforcement

To check the lable of a file or a directory.

#ls -lZ

To check the lable of a process (ex: httpd).

#ps axZ | grep httpd

To check the label of a socket (ex: httpd).

#netstat -taZ | grep httpd

Checking errors related to SELinux.

#journalctl

change type in a label.

#chcon -t <type> FILENAME

Where the context stored.

#etc/selinux/targeted/contexts/files/file_contexts

To set boolean.

#setsebool -P bool_name on/off

To check boolean.

#getsebool -a

#semanage boolean -l




