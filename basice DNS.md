### What is DNS?

DNS or domain name system is the internet service that translates human-friendly 
domain name like www.example.com into machine- readable ip addresses.

#setup our own webserver

Installation (centos or redhat)

package we need to install.

#sudo yum install httpd

#systemctl start/stop/status httpd (httpd is the process or service name)

#ifconfig


Enable the service in firewall.

#firewall-cmd --add-service=http --permanent

#firewall-cmd --reload

webserver config file under.

#/var/www/html/index.html

#/etc/httpd/conf/httpd.conf 

Package we need to install for the DNS is bind (berkeley internet name domain)

#sudo yum install bind bind-utils

#systemctl start/stop/status named (named is the process or service name)

Enable the service in firewall.

#firewall-cmd --add-service=dns --permanent

#firewall-cmd --reload

DNS config file under.

#/etc/named.conf

Directory where all the zone files are present where you define hostname to ip

#named-checkconf ---> to check the file is correct or not.

#/var/named -> in side we will create file.

#touch mywebzon.com.fzone

we need to edit this file mywebzon.com.fzone.

for learning purpose //bind9.readthedocs.io in this webside we will get info how to edit zones or such thing .

#named-checkzone  mywebzon.com.fzone

#systemctl restart named

#systemctl status named

#vi /etc/resolve.conf  #in this file we will do entery for nameserver.








 

