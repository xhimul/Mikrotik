# Per Connection Queue (PCQ)

## Step 1 (Add two mangle rules):

##### IP > Firewall > Mangle > 
General > Chain: prerouting, In-interface: LAN\
Action: mark packet, New Packet Mark: client_upload, Passthrough: Check

##### IP > Firewall > Mangle > 
General > Chain: prerouting, In-interface: WAN\
Action: mark packet, New Packet Mark: client_download, Passthrough: Check


## Step 2(Add two Queue Type):
Queues > Queue Typs > Name: pcq_download, Kind: pcq, Rate: 10M, Classifier: Dst. Address\
Queues > Queue Typs > Name: pcq_upload, Kind: pcq, Rate: 10M, Classifier: Src. Address

## Step 3 (Add two Queue Tree):
Queue Tree > Name: queue_pcq_download, Parent: global, Packet Marks: client_download, Queue Type: pcq_download\
Queue Tree > Name: queue_pcq_upload, Parent: global, Packet Marks: client_upload, Queue Type: pcq_upload
