
# linux package management

## Package management

	- Installing
	- Upgrading
	- Deleting
	- View Package Info
	- Packages config
	
## Manage software using YUM/DNF and RPM for your red hat-based linux systems
   like centos
   
   APT for Debian based, Ubuntu, Kali Linux etc
   
## Yum yellow-dog updater modified

	- Yum is the primary package management tool for redhat 
 
	- yum performs dependency resolution when installing updating and removing
	  software packages
	  
	- yum can manage packages from installed repositories in the system or from rpm packages

## YUM Commands 

	- How to install and remove a package
	
	#yum install ngninx -y 
 
	#yum remove ngninx
	
	- How to upgrade or update a package
	
	#yum upgrade package
 
	#yum update package
	
	
	### What is the different between yum update and yum upgrade

Upgrade : will delete the old packages.

Update : keep the old packages, we can rollback.

#### Yum command.

 - you can see all the options using.
 
 #yum -option
 
 - To check the available update for packages.
 
 #yum check-update
 
#### Packages rollback.

 - To see the past work done related to packages, which will show you the activity with data and time.
 
 #yum history
 
 - We can simply undo or redo any action using.
 
 #yum history undo/redo <id>
 
 example:
	
		#yum history undo 8
		
		#yum history redo 8
		
		
#### RPM redhat package manager.


 - Using RPM you can install , uninstall and quary individual software package.
 
 - issue: it can not manage dependency resolution like yum.
 
 - RPM maintains a database of installed packages, which enables powerful and fast quaries.
 
 
 - To install, upgrade or delete an rpm package using RPM.
 
 #rpm -i package-file
 
 #rpm -U package-file
 
 #rpm -ivh package-file
 
 #rpm -evh package-fie
 
 
 (v-verbose, h for hash to show progress).

  - To quary all the installed packages.
 
 #rpm -qa
 
 - To quary all the installed packages if we need any specefic package.
 
 #rpm -qa | grep ksh 
 
 - More info about the package.
 
 #rpm -qi <package_name>
 
 - Info about the config files for package.
 
 #rpm -qc <package_name>
 
 #### DNF dendified yum.
 
 #sudo dnf list available
 
 #sudo dnf list install
 
 #sudo dnf update/upgrade 
 
 #sudo dnf install package.name
 
 #sudo dnf remove package.name 
 
 #sudo dnf info package.name
 
 #sudo dnf search package
 
 example:
 
	#dnf list available | wc -l
	
	#dnf list installed | grep ksh
	
	#dnf info ksh
	
	#dnf install http
	
	#dnf remove http
	
	APT.
	
	#apt install package_name
	
	#apt remove package_name
	
	#apt autoremove (to remove the dependencies)
	
	#apt update (to update the repo)
	
	#apt-cach search apache
 
 
 
 
