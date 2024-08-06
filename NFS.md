## NFS

Network file system.

A network protocal for distributed file system.

Using this a user on the client computer, can access the files on server side like as they are accessing locally.

NFS Configuration Setup.

We need to setup in two parts

- Clinet side configuration

- Server side Configuration



### Server side Configuration.

- To install NFS Packages.

#yum install nfs-utils libnfsidmap -y 

- Enable and start the NFS services

#systemctl enable rpcbind, nfs-server

#systemctl start rpcbind, nfs-server, rpc-statd, nfs-idmap

#systemctl status rpcbind, nfs-server, rpc-statd, nfs-idmap

- create a directory for NFS and give all the permissions

#mkdir /server/apps

- modify the /etc/exports file and add new shared filesystem 

#/apps <IP_allow>(rw, sync, no_root_squash)

- exportfs -rv

### Clinet side Configuration.

- To install NFS Packages

#yum install nfs-utils rpcbind 

- Enable and start the rpcbind service 

#systemctl enable rpcbind

#systemctl start rpcbind

#systemctl status rpcbind

- To stop the firewall

#systemctl stop firewall / iptable

- show mount from NFS Server

#showmount -e <IP of server side>

- To check ip 

#ifconfig

- Create a mount point (a directory)

#mkdir /mnt/apps

- Mount the NFS file system

#mount <IP_server>:/server/apps /mnt/apps

