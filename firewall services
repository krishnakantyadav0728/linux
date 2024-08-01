**Linux Firewall**
===============
What is a firewall
A firewall is a network security system that monitors and controls incoming and outgoing network
traffic based on the rules defined

basically used to determine and block untrusted network to access out system

types of firewall

1.software based
running on operating system

2.hardware based 
A dedicated appliance with firewall software between two different networks (mostly used by network team)

==============
Tools on linux for managing firewall
1.iptables
2.firewalld - newer version of centos, redhat. fedora etc.

==========
listing adding deleting firewalld rules

===========
check if firewalld service is installed 
#rpm -qa | grep firewalld

#systemctl start/enable firewalld
#systemctl stop/disable firewalld
#systemctl status firewalld
#systemctl restart firewalld


=============
check the rules of firewalld
#firewall-cmd --list-all

listing of all the services firewalld is aware of 
#firewall-cmd --get-services

To reload the config of firewalld
#firewall-cmd --reload

firewall has multiple zones, to get list-all
#firewall-cmd --get-zones

To see the lsit of active zones
#firewall-cmd --get-active-zones

To get firewall rules for a specific zones
#firewall-cmd --zone=public --list-all

================================

To add or remove a service
#firewall-cmd --add-service=(name of service)
#firewall-cmd --remove-service=(name of service)
example:
	#firewall-cmd --list-all
	#firewall-cmd --get-services | grep http
	#firewall-cmd --add-service=http
	#firewall-cmd --list-all
	#firewall-cmd --remove-service=http
	
To add or remove a service permanently 
#firewall-cmd --add-service=(name of service) --permanent 
#firewall-cmd --remove-service=(name of service) --permanent 
example:
	#firewall-cmd --add-service=http --permanent 
	#firewall-cmd --remove-service=http --permanent 
	#systemctl restart firewalld
	
To add or remove a port

#firewall-cmd --add-port=20201/tcp
#firewall-cmd --remove-port=20201/tcp

or
#firewall-cmd --add-port=20201/tcp --permanent
#firewall-cmd --remove-port=20201/tcp --permanent


To block incoming traffic from an ip 
#firewall-cmd --add-rich-rule='rule family="ipv4" source address="192.16.3.20" reject'
 
To block outgoing traffic to a ip or URL
example:
	#firewall-cmd --direct --add-rule ipv4 filter OUTPUT 0 -d 157.240.242.35 -j DROP
	
To block ICMP incoming traffic
#firewall-cmd --add-icmp-block-inversion 



