NAT = 
Source NAT      = Outgoing Traffic
Destination NAT = Incoming Traffic

Firewall Zones


Inside (Private System)
DMZ (Semi Protected Area)
Outside (Unprotected Networks)

firewall are used to control traffic between zones

Layer 4 - Protocol and port
Layer 3 - Source and destination IP addresss
Rules - Processed from top to down
Rules order is important
Last rule denies all


example :
    access-list 100 permit tcp any host 192.0.0.1 eq 25
    access-list 100 permit tcp any host 192.0.0.1 eq 110
    access-list 100 deny ip any host 192.0.0.1
    access-list 100 deny udp any any eq 53 
    access-list 100 permit ip any any


Stateful firewall tracks connection state
Response traffic is allowed
Stateless firewall require rules in both direction


Deep packet inspection
Signatures must be upto date

if 1 firewall doesnt catch:
    another firewall

if malware inside can stop the firewall

third paty systems /Not firewall 
Windows : Windows firewall
Linux : iptables

Host based firewall runs on the OS
Reside in the attack surface
Provide defense in depth


IDS - Intrusion Detection System
IPS - Intrusion Prevention System

Signature Based
    Strings of bytes matching known malware or known attack. Can be downloaded 

Behaviour Based
    Determine normal baseline traffic
    Watch for unusual traffic


Firewall And DDOS

VLAN segmentation

Use different Segments for different security zones
You can enforce rules on traffic between segements, not within segements

Microsegmentation


