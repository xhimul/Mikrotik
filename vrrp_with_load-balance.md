# R1:
Add WAN IP
### Add LAN IP: 
IP > Address > ether2 > 10.0.201.1/24

##### Add VRRP:
Interface > VRRP > vrrp1 >Interface: ether2 > VRID: 10 > Priority: 100\
Interface > VRRP > vrrp2 >Interface: ether2 > VRID: 20 > Priority: 140\
\
IP > Address > vrrp1 > 10.0.201.253/24\
IP > Address > vrrp2 > 10.0.201.254/24\



# R2:
Add WAN IP
### Add LAN IP: 
IP > Address > ether2 > 10.0.201.2/24\

##### Add VRRP:
Interface > VRRP > vrrp1 >Interface: ether2 > VRID: 10 > Priority: 90\
Interface > VRRP > vrrp2 >Interface: ether2 > VRID: 20 > Priority: 150\
\
IP > Address > vrrp1 > 10.0.201.253/24\
IP > Address > vrrp2 > 10.0.201.254/24\


#### AP1 > 10.0.201.3/24 GW: 10.0.201.253
#### AP2 > 10.0.201.4/24 GW: 10.0.201.254 
