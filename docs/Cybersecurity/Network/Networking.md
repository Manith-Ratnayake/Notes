Protocols are agreed ways to communicate 


IP
  

---------------------------------------------------------------------------
Version   IHL    Type of Service   Total Length
------------------------------------------------------------------------------
Identification    IP Flags   Fragment Offset
-----------------------------------------------------------------------------
Time to Live (TLI)    Protocol   HeaderChecksum
-----------------------------------------------------------------------------
Source Address
-------------------------------------------------------------------
Destination Address
------------------------------------------------------------------
IP option ()
------------------------------------------------



TCP

--------------------------------------------------------------------------
Source Port               Destination Port
-------------------------------------------------------------------------
Sequence Number
-----------------------------------------------------------------
Acknoledgment Number
----------------------------------------------------------------
                                                      Window size
-------------------------------------------------------------------
Checksum            Urgent Pointer
-------------------------------------------------------
Options                   Padding
-------------------------------------------------


DNS have 4 sectors  

1. Dense cache : you dont have to again to look the IP address
2. Resolvers : 
3. Name Servers
4. Name Space



Every DNS has an public an private key.


Automobile use several different protocols to communicate between multiple micro controllers such as sensors, gauges, actuators etc

Controll Area Network (CAN)

It was designed by Germany, communication with vehicle micro controllers and devices without a host computer

CAN runs on 2 wires, 
  CAN High
  CAN Low

CAN Message Type 

 Data Frame : only used for data transmission 
 Remote Frame 
 Error Frame 
 Overload Frame