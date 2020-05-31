# Virtual Router Redundancy Protocol (VRRP)
## R1:
### Add WAN IP:
IP > Address > ether1 > XX.XX.XX.XX/XX
### Add LAN IP: 
IP > Address > ether2 > 10.0.201.2/24

##### Add VRRP:
Interface > VRRP > vrrp1 >Interface: ether2 > VRID: 10 > Priority: 100

### Add VRRP IP:
IP > Address > vrrp1 > 10.0.201.1/24


## R2:
### Add WAN IP:
IP > Address > ether1 > XX.XX.XX.XX/XX
### Add LAN IP: 
IP > Address > ether2 > 10.0.201.3/24

##### Add VRRP:
Interface > VRRP > vrrp1 >Interface: ether2 > VRID: 10 > Priority: 110

### Add VRRP IP:
IP > Address > vrrp1 > 10.0.201.1/24


##### AP1 > 10.0.201.3/24 GW: 10.0.201.1/24
##### AP2 > 10.0.201.4/24 GW: 10.0.201.1/24
