###### IP > Firewall > NAT > Add
- General > Chain: dstnat | Dst. Address: Public IP | Protocol: 6 (tcp) | Dst. Prot: 4370
- Action > Action: dst-nat | To Address: Private IP | To Ports: 4370
