If computer became and apartment

IP address is the street address
Port number is the room number

Classes of IP address
  class A : 0.0.0.0 - 127.255.255.255
  class B : 128.0.0.0 - 191.255.255.255
  class C : 192.0.0.0 - 223.255.255.255

Public IP address have 4.3 billion 


Class private address
  class A : 10.0.0.0 - 10.255.255.255
  class B : 172.16.0.0 - 172.16.255.255
  class C : 192.168.0.0 - 192.168.255.255

DHCP - Dynamic Host Configuration Protocol


On LAN, we use private address
 gives an IP address for fixed amount of time DHCP server which is known as "lease"

NAT (Network Address Translation)
Internal private IP addresses are converted to external Public IP address


How many ports are available: 2 ^ 16 = 65, 536
first 1024 are common addresses


Protocol?
are simply an agreed upon way to communicate 

Protocol are rules are Request for Comments

There are many protocol [TCP, UDP, IP, FTP, SMTP]

IP used to define the source and destination IP address of a packet as it traverses the internet.


Subnetting 


netstat -> network statistics
see specific connection  
  netstat -a | grep http


ss is even more detailed version of netstat




Network sniffer - packet analyser, protocol analyzer, network traffic analyzer



Fliter tcp Flags 

  tcpdump 'tcp[tcpflags] == tcp-syn'
  tcpdump 'tcp[tcpflags] == tcp-ack'
  tcpdump 'tcp[tcpflags] == tcp-fin'
  tcpdump 'tcp[tcpflags] == tcp-rst'
  tcpdump 'tcp[tcpflags] == tcp-urg'
  tcpdump 'tcp[tcpflags] == tcp-urg'
  

tcpdump not host 192.12.192.12
tcpdump --vvAls0 | grep 'User-Agent'

-------------------------------------------------------


firewall can either hardware or software


IpTable
  : built up on main things known as 
    - tables
    - chains
    - targets


There are 4 tables:
  
  Filter  - default table is none other speicified 
  NAT     - rewrite source/destination of packets
  Mangle  - packet alternation such as modifying the TCP header
  RAW     - configuration exemptions from connection tracking 

Chains
 List of rules in the table

 - INPUT = packets designed for coming to the system 
 - FORWARD = packets designed for leaving the system
 - OUTPUT = packets designed for routed through local system

 Match : packet meets condition 


Targets 
  : Accept
  : DROP
  : LOG
  : REJECT
  : RETURN


sudo iptables -L 
sudo iptables -h 


sudo iptables -A INPUT -s 192.168.0.0/24  -j DROP

sudo iptables -A OUTPUT -p 


to flush the iptable we can use 
  iptable -F