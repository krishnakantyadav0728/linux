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
 
 
 
 
