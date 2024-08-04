# NETSTAT ( network monitoring and troubleshooting )

### netstat command

netstat is a command line network utility that displays:

- network connections for TCP, UDP

- routing tables

- a number of network interface

- network protocol statistics

example:

 To identify no of connection on a given port or IP.

 #netstat -putan | grep :22
 
( t-tcp, u-udp, n-numerical addr, l-listening port, p-PID programname)

To see all the sockets.

#netstat -a
 
list all the TCP ports.

#netstat -at

list all the TCP v4 ports.

#netstat -4at

list all listening ports.

#netstat -l

list all the UDP ports.

#netstat -au

#netstat | more

#netstat -au | more

#netstat -l | more

#netstat -atln | more  ===numerical format

#netstat -r ===routing table info

To get the all the server inerface.
 
#netstat -i 

which port a process is using.

#netstat -ap | grep <process name)

how to see statistics by protocol.

#netstat -s







