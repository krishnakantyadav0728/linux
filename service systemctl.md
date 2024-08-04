#SYSTEMCTL

### what is systemctl

It is used to control the status of the sevices. control systemctl system. 

example:
 
 #systemctl status <service_name>
 
- Start or stop a service.

#sudo systemctl start/stop <service_name>

- To check the status

#sudo systemctl status <service_name>

- To restart the service

#sudo systemctl restart <service_name>

- why we are enable the service

-Enabling a service causes the system to start the service upon reboot or whenever a computer starts up 

- the enable subcommand does not start the particular service immediately

- you need admin rights


- TO enable and start at same time.

#sudo systemctl enable --now sshd

- To check if a service is enabled?

#sudo systemctl is-enable sshd

- disable a service

- one can manually start the service

# sudo systemctl disable <service_name>


- To prevent the service to start

#sudo systemctl mask <service_name>

- To check if a service is enabled

#sudo systemctl unmask <service_name>


- computer control commands

#systemctl poweroff

#systemctl reboot

#systemctl -i reboot (ignoring logged in users)

- TO List the socket in memory avaliable for interprocess communication (Ipc)

#systemctl list-sockets

#systemctl --show-types list-sockets

#systemctl --show-types list-sockets 'systemd*'

#systemctl --show-types list-sockets --all



