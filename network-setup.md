Router0 - 1941

Router Interfaces:
Gi0/0: 210.3.14.1
Gi0/1: 168.90.0.1


-------------------------- LAN 1
Switch1 - 2960-24TT - 210.3.14.1
Server0 - Server-PT - 210.3.14.14
PC0 - PC-PT - 210.3.14.13
PC1 - PC-PT - 210.3.14.12
PC3 - PC-PT - 210.3.14.15
Laptop0 - Laptop-PT - 210.3.14.11



-------------------------- LAN 2

Switch2 - 2960-24TT - 168.90.0.1
Server1 - Server-PT - 168.90.0.13
Server2 - Server-PT - 168.90.0.12
PC2 - PC-PT - 168.90.0.11
PC4 - PC-PT - 168.90.0.14


DHCP and Explanation

Router(config)# ip dhcp pool VLAN1 - created a DHCP pool of available addresses
Router(dhcp-config)# network 168.90.0.0 255.255.0.0 - specified the network range of the pool
Router(dhcp-config)# default-router 168.90.0.1 - assigns the default gateway for devices
Router(dhcp-config)# exit - exits


Router(config)# ip dhcp pool VLAN2 - created a DHCP pool of available addresses
Router(dhcp-config)# network 210.3.14.0 255.255.255.0 - specified the network range of the pool
Router(dhcp-config)# default-router 210.3.14.1 - assigns the default gateway for devices
Router(dhcp-config)# exit - exits