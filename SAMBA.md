# SAMBA

A Linux utility or tool to share Linux files and print services to other OS.

Using server message block (SMB) and common internal file system (CIFS) Protocols.

Serever side configuration.

- To insatll samba packages.

#yum install samba samba-client samba-common

- Enable samba through firewall

#firewall-cmd --permanent --zone=publice --add-service=samba
#firewall-cmd --reload
