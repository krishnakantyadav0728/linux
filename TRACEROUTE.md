#TRACEROUTE

### what is traceroute

Tracks the route packets on how the data travels on internet from your computer to destination.

The only required parameter is the name or ip address of the destination host.

To install traceroute.

#yum install traceroute

$traceroute IP

- Default packet length is 60byte to change it

#traceroute google.com 80

- Default no of packet per hop is 3, to change it 

#traceroute -q 1 google.com

- Default port is 33489, to change it

#traceroute -p 21102 google.com

- To use IPV6 or IPV4

#traceroute -4/6 google.com

- To route through gate 

#traceroute -g 172.168.43.45 google.com
