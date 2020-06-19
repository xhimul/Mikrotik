#### Router1 [turnk port- ether5]:
create bridge_vlan  
add trunk port in bridge (ether5)\
\
interface > vlan100 (id-100, int-bridge_vlan)\
interface > vlan200 (id-200, int-bridge_vlan)\
\
id > address (ip-10.0.100.1/24, int-vlan100)\
id > address (ip-10.0.200.1/24, int-vlan200)\
\
id > dhcp server > dhcp setup (int-vlan100)\
id > dhcp server > dhcp setup (int-vlan100)\
\

#### Router2 [turnk port- ether1 [uplink], vlan100-ether2&3, vlan200- ether4&5]:
create bridge_vlan100
create bridge_vlan200\
\
interface > vlan100 [id-100, int-ether1 (trunk port)]\
interface > vlan200 [id-200, int-ether1 (trunk port)]\
\
bridge > add port > (bridge-bridge_vlan100, int-ether2)\
bridge > add port > (bridge-bridge_vlan100, int-ether3)\
bridge > add port > (bridge-bridge_vlan100, int-vlan100)\
\
bridge > add port > (bridge-bridge_vlan200, int-ether4)\
bridge > add port > (bridge-bridge_vlan200, int-ether5)\
bridge > add port > (bridge-bridge_vlan200, int-vlan200)
