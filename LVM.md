### LVM logical volume manager

LVM is used to manage volume and disk on the linux server.

Logical volume manager allow disk to be combined together.

	example of LVM
	
	like partition of disk in windows C, D drive similarly we can do the same in the  linux.
	
	- single disk can we divided into different partition.
	
	- multiple disk combined and group them into .
	
	one -> then change it into different partition.
	
	Advantage of LVM.
	
	- In case of disk is running  out of space you can add new disk without breaking partitions of your file system.
	
	Possibilities of LVM
	
	- new space can be created on  a server for new project.
	
	- In case of low disk space increase the space
	
	- In case of extra  space  allocation to a partition capacity can be reallocated ( reduce capacity in one volume group 
	  and add it to another).
	  
	 ##### Steps of LVM for adding new space
	 
	 - Install a new hard disk drive
	 
	 - how to check disk is added
	 
	 #fdisk -l 
	 
	##### partition using 'fdisk'.
	 
	 steps:
	 
	 #fdisk /dev/sdb
	 
	 - choose n to create new .
	 
	 - choose p to create a primary partition.
	 
	 - choose which number of partition we need to create.
	 
	 - press enter twice to use full sapce of the disk.
	 
	 - we need to change a type of newly created partition type t.
	 
	 - which number of partition need to change  choose the number which we created its. 1
	 
	 - here we need to change the type we need to create LVM so we going to use the type 
	   code  of LVM as 8e , if  we do not know the type code press L to list all type codes.
	 
	 - print the partition what we created to just confirm.
	 
	 - here we  can see the ID as we linux LVM.
	 
	 - write the changes and exit fdisk.
	 
	 
	m = for help.
	
	n = for new partition 
	
	p = for primary
	
	#how to change partition type 
	
	t = for type 
	
	L = for list all code
	
	w = for write table to disk
	
	
	designate physical volume (PV) so that it will be available to LVM as storage  capacity.
	
	command to create pv.
	
	#pvcreate /dev/sdb1
	 
	#pvdisplay  -> to display the create pv
	
	
