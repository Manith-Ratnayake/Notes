
1. What is cybersecuity
• Cybersecuirty is the combination of process, practicies and technologies to protect networks, computers, programs, data and information from attack, damage or unauthorized access

2. What do you have on your home network?
• A home network gives you test enviornment for experimentation. Active directory domain controller, a dedicated firewall appliances and a net attached toaster- as long as you are learning and fidding with it, that's what matters


3. What is encryption? why is it important?
• A process of converting data into an unreadable from to prevent unauthorized access and thus ensuring data protection


4. Tell me the difference between symmetric and asymeteric encryption
------------------------------------------------------------------------
Basis      |   Symmetric Encryption        |   Asymmetric Encryption
--------------------------------------------------------------------------
Encryption      Single key for both encryption     Use different keys for encryption 
key             and decryption                     and decryption

Performance     Encryption is fast but comparatively    Encryption is slow due to hig
                 more vulnerable                        computation

Algorithms        DES, 3DES, AES, and RC4               Deiffie-Hellman, RSA

Purpose            Used for bulk data transmission    Often used for securely exchaning secret keys





5. What is CIA triad?
• The CIA triad for information secuirty, provides a baseline standard for evaluating and implementing information secuirty - irrespective of the system and/or organization
in question


6. What do you understand by risk, vulnerability & threats in a network?
Threat  -  Refers to someone with the potential to do harm to a system or an organization
Vulnerability 
Refers to a weakness of an asset(resource) that can be exploited by one or more attackers(threat actors). In other   words, it is an issue or bug that allows an attack tobe successful
Risk  -   Refers to the potential for loss or damage when a threat exploits a vulnerability



7. How do you report Risks?
• Risk needs to be assessed first before it can be reported. There are two ways you can analyse risk. It can be either Quantitative or Qualitative
• This approach is suitable for both technical and business guys
• The business guys will see the probable loss in numbers while the technical guys will monitor and assess the impact and frequency. Depending on the audience, the risk can then be reported



8. How do you differentiate between IPS and IDS system?
IDS = Intrusion Detection System
IPS = Intrusion Prevention System
IDS just detect the intrusion and leaves the rest to the administrtor for assessment
and evaluation or any further action
IPS detect the intrusion and takes necessary action to further prevent intrusion
Also there is a differnce in the positioning of devices in the network. Although they work on the same concept, the placemnt is different


9. What do you know about Cybersecuirty Frameworks?
* PCI DDS 
* ISO 27001/27002
* CIS 
* NIST


10. What is weak information Security
• Information secuirty policy is considered to be weak if does not meet the criteria 
of an effective one. The criteria include: Distribution, review, Comprehension, and uniform 
Information security is weak if:
-> The policy has not been made readily available for review by every employee within the organization
-> The organization is unable to demonstrate that employees can review the policy document
-> The organization is unable to demonstrate that employees understand the content of the policy documemt



11. What's the better approach of setting up a firewall?

* Username/password: Modify the default password for your firewall device
* Remote Administration : Disable the feature of remote administartion from outside the network
* Port forwarding: For certain application to work properly, such as web server of FTP server, you need to configure appropiate port forwarding
* DHCP server : INstalling a firewall on a network with an existing DHCP server will cause conflicts unless the firewall's DHCP server is disabled
* Logging : In order to troubleshoot firewall issues or potential attacks, you want to make sure to enable logging and understand how to view the logs
* Policies : you want to have solid secuirty policies in place and make sure that your firewall is configured to enforce those policies



12. Can you explain SSL encryption?
SSL (Secure Socket Layer)
• is a protocol which enables safe conversation between two or more parties. It is designed to identify and verify that the person you are talking to on the other end is who they say they are.

HTTPS
• is HTTP combined with SSL which provides you with a safer browsing experience with encryption. Sp, this a very tricky questions but SSL wins in terms of secuirty


13. Which one is more secure SSL or TLS?
SSL 
• is a meant to verify the sender's identify but it doesn't search for any more hazards than that. SSL can help you track the person you are talking to but that can also be trciked at times
TLS 
• is another identification tool just like SSL, but it offers better secuirty features. It provides additional protection to the data and hence SSL and TLS are often used together for better protection


14. What are Salted Hashes?
• Salt is a random data. When a properly protected password system receives a new password, it creates a hash value of that password, a random salt value, and then combined value is stored in its database. This helps defend against dictionary attacks and known hash attacks
Example : A person use the same password on two different systems and they are being used using the same hashing algorithm, the hash value would be same, howvever if even one of the system uses salt with the hashes, the value will be different


15. How identity theft could be prevented?
* Ensure strong and unique password 
* Avoid sharing confidential information online especially on social media
* Shop from known and trusted websites
* Use the latest version of the browesers
* install advanced malware and spyware tools
* Use specialized secuirty solutions against finacial data
* Always update your system and the software
* Protect your SSN 


16. How can you prevent Man in the middle (MITM) attack?
• MITM attacks happens when a communication between two parties(system) is intruded or intercepted by an outside entity
First method
• To prevent this attacks would be to have encryption (preferably public key ecncryption) between both the parties. This way, they both will have an idea with whom they are talking because of the digital verification
Second method
• To prevent this, it is best to avoid open WIFI networks and if it is necessary then use plugins like HTTPS, Forced TLS etc.


17. State differences between encoding, hahsing and encryption

Encoding:
Converts the data in a desired format required for exchange between different systems
Hashing 
Maintains the integrity of a message or data. Any change done any day could be noticed
Encryption
Ensures that the data is secure and one needs a digital verification code or image in order  to open or access it


18. What steps will you atek to a secure a server
• Secure servers use the Secure Socket Layer(SSL) protocol for data encryption and decryption protected data from unauthorized interception
4 stpes
1) Making sure that have a secure password for root and administration users
2) Making a new users on your systems. These will be useres use to manage the system
3) Remove remote access from the default root/adminsitartor accounts
4) The next step is to configure firewall rules for remote access

19. What is DDos attack? How is it mitigated?
• DDoS stands for distributed denial of services. When a network is flooded with large number of requests which is not recognized to handle making the server unavilable to the legitimate requests
• DDoS can be mitigated by analysing and filtering the traffic in the scrubbing centers. The scrubbing centers are centralized data cleansing station wherein the traffic to a website is analysed and the malicious traffic is removed


20. Why do you need DNS monitoring?
• The domain Name system allotes your website under a certain domain that is easily recognizable and also keep the information about the other domains names. It works like a directory for everything on the internet. Thus, DNS monitoring is very important since you can easily visit a website without actually having to memorise their IP address.

21. What is a three-way handshake
• The TCP three-way handshake is the method used by TCP set up a TCP/IP connection over an internet Protocol based network.
• TCP's three way handshaking techniques is often reffered to as SYN-SYN-ACk (or more accurately SYN, SYN-ACK, ACK) because there are messages transmitted by TCP to negotiate and start a TCP session between two computers


22.

23. How often should you perfrom Patch management?
• Patch manage should be done as soon as it is released. For windows, once the patch is released it should be applied to all machines not later than 1 month. Same goes for network devices, patch it as soon as it is released. Proper patch management process should be followed


24. What do you know about application secuirty?
• Application secuirty is the practise of improving the security of application using software, hardware and other procedral methods
• Countermeasures are taken to ensure application security, the most common being an application firewall is that limits the execution of files or the handlinf of data by specific installed programs


25. Differntiate between penetration testing and software testing?
Peneration Testing = helps identify and address the security vulenrabilities
Software Testing = Focuses on the functionality of the softwares and not the secuirty aspect

26. When to use tracert/traceroute?
• Small TTL values are transmitted through packets via traceroute. This prevents the packets from getting into loops. In case you can't ping the final destination, tracerout will help to identify where the connection stops or gets broken, whether it is firewall, ISP, router etc 

27. Tell me about common cyber threats
* Malware
* Phising
* Man in the Middle
* Maladvertising
* DDoS
* Rouge Software
* Drive bt Downloads

28


29. How would you reset a password-protection BIOS configuration
• Since BIOS is a pre boot system it has its own storage mechanism for its settings and preferences. In the classic scenario, simply popping out the CMOS (complementary metal-oxide-semiconductor) battery will be enough to have the memory storing these settings lose its power supply, and as a results it will lose its settings
• The simplest way by far however is this: if the BIOS has come from the factory with a default password enabled, try `password`


30. What is cross site scripting or XSS
• XSS refers to client side code injection attack wherein an attacker can execute malicious into a legitimate website or web application
• XSS is amongst the most rampant of web application vulnerabilities and occures when a web application makes use of unvalidated or unencoded user input within the output it generates



31. What is data protection in transit vs data protection at rest?
Data protection in transit
• This when data isgoing from server to client
• Effective data protection measures for in transit data are critical as data is less secur when in motion
Data protection at rest
• This is when data is just sitting there in its database or on its hard drive
• Data at rest is sometimes considered to be less vulenrable than data in transit


32. Tell me the differences between cybersecuirty and network security
Cybersecuirty
• Describes that the policies and procedures implemented by a network administrator to avoid and keep track of unauthorized access, exploitation, modificationm, or denial of the network and network resources

Network Security 
• Process and practices designed to protect networks, computers programs and data from attack, damage or unauthorized access. In a computing context, secuirty includes both cyber security and physical security

33. How will you prevent data lekage

* Data lekage is when data gets out of the organization in an unauthorized way
* Data can get leaked through various ways - emails, prints, laptop getting lost unauthorized uplaod of data of data to public portals, removable drivers, photographs etc
* A few controls can be restricting upload on internet websites, following an internal encryption solution, restricting the mails to internal networks, restricts on printing confidentails data etc



34. What is an ARP and how does it work?
* Address Resolution Protocol(ARP) is a protocol for mapping an Internet protocol address(IP address) to a physical machine address that is recognized in the local network
How it works?
* When an incoming packet destined for a host machine on a particular local area network arrives at a gateway asks the ARP program to find a physical host or MAC address that matches the IP address.
* The ARP program looks in the ARP cache and, if it finds the address, provides it so that the packet can be convereted to the right packet length and formats and sent to the machine
* If no entry is found for the IP address, ARP broadcast a request packet in a special formats to all the machines on the LAN to see if one machine knwos that it has that IP address asscociated with it


35. What is 2FA and how can it be implemented for the public websites?
• An extra layer of secuirty that is known as "multi factor authentication"
• Requires not only a password and username but also something that only, and only, that user has on them 
ex: Piece of information only they should know or have immediately to hand such as a physical token 
• Authenticator apps replace the need to obtain a verification code via text, voice call or email


36. What techniques can be used to prevent brute force login attack
• Here the attacker tries to determine the password for a target (services/system/device) through a permutation of fuzzing process
• As it is a length task, attackers usually employ a software such as fuzzer, to automate the process of creating numerous passwords to be tested against a target
• In order to avoid such attacks-passwords best practices should be followed mainly on critical resources like servers, routers, exposed services so on


37. What is cognitive cybersecurity
• Application of AI technologies patterned on human thought processes to detect threats and protect physical and digital systems
• Self learning security systems use data mining, pattern recognition and natural langauge processing to simulate the human brain, albeit in a high powered computer model


38. What is port blocking withing LAN?
• Restricting the users from accessing a set of services within the local area network is called port blocking
• Stopping the source to not to access the destination node via ports as application works on the ports so ports are blocked to restrict the access filling up the security holes in the network infrastructure


39. What is the differences between VPN and VLAN?

VPN
• related to remote access to the network of a company
• used to connect two points in a secured and encrypted funnel
• Saves the data from prying eyes while in transit and no one on the net can capture the packets and read the data

VLAN
• helps to group workstation that are not within the same location into the same broadcast domain
• Basically a means to logically segregate networks without physically segregating them with various switches
• Does not involve any encryption technique but it is only used to slice up your logical network into different sections for the purpose of management and security


40. What protocols falls under TCP/IP internet layer?

TCP/IP Layer                                            Protocol Examples
Application                     NFS, NIS+,DNS, telnet, ftp, rlogin, rsh, rop, RIP, RDICS,SNMP
Transport                       TCP, UDP
Internet                         IP, ARP, ICMP
Data link                       PPP, IEEE 802 2
Physical Network            Ethernet(IEEE 802.3) Token Ring, RS-232 other
