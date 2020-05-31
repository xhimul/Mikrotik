# R1:
### Add WAN IP:
IP > Address > ether1 > XX.XX.XX.XX/XX
### Add LAN IP: 
IP > Address > ether2 > 10.0.201.1/24

### Add VRRP:
VRRP > R1_VRRP1_Master >Interface: ether2 > VRID: 10 > Priority: 100\
VRRP > R1_VRRP2_Slave >Interface: ether2 > VRID: 20 > Priority: 140
### Add VRRP IP:
IP > Address > R1_VRRP1_Master > 10.0.201.253/24\
IP > Address > R1_VRRP2_Slave > 10.0.201.254/24

### DHCP Server:
IP > DHCP Server > [Interface: LAN_ether2] > GW: 253 Range: 101-200



# R2:
### Add WAN IP:
IP > Address > ether1 > XX.XX.XX.XX/XX
### Add LAN IP: 
IP > Address > ether2 > 10.0.201.2/24

### Add VRRP:
VRRP > R2_VRRP1_Slave >Interface: ether2 > VRID: 10 > Priority: 90\
VRRP > R2_VRRP_Master >Interface: ether2 > VRID: 20 > Priority: 150
### Add VRRP IP:
IP > Address > R2_VRRP1_Slave > 10.0.201.253/24\
IP > Address > R2_VRRP_Master > 10.0.201.254/24
### DHCP Server:
IP > DHCP Server > [Interface: LAN_ether2] > GW: 254 Range: 101-200


#### AP1 > 10.0.201.3/24 GW: 10.0.201.253
#### AP2 > 10.0.201.4/24 GW: 10.0.201.254 
