What is active directory autentication 

It is a system in windows that checks if users, devices and services are allowed to access the AD Network 
AD authentication helps IT Teams easily manages   users,permission,Devices, User setting with a feature called AD Group policy
AD autentication let users sign in just once and access different parts of the company's network without having to `Sign In Again` (SSO)

Before AD sutentication there were other systems called LAN Manager, NT LAN Manager (LM, NTLM)
But they used weak methods to protect information
AD authentication was created to fix these issues. 
AD Authentication uses two standards
    - Kerberos
    - Lightweight Directory Access Protocol

With Kerberos-based AD authentication
You only need to Log In once to access multiple things on the network

Instead of sending your login details over the network. Kerberos creates a special key just for you
This key lasts for a certain length of time, while it's active you won't have to keep re entering your password 
Kerberos also makes sure you only access things you're allowed to by creating a token with all the permission and rights for the account

LDAP 
Simple Authentication - Just require your login detials to connect to the server
Simple Authentication and secuirty layer (SASL)  - Adds other authentication requiremenrts 
    Because its separate the way you prove yourself from the actual applications you're using

There are two ways to connect linux to active directory
LDAP  - Admin reconfigure the device to access plugable authentication module(PAM)
SAMBA - 

MAC OS 
AD connect using
    - LDAP
    - AD connector

To make AD work on some MAC, IT Teams  have to use weaker  secuirty measures 

Since AD was developed to focus on Winodws, combining it with other OS and cloud based systems is not very efficient
Instead of using 1 system IT system using different systems end up being more complex  and time consuming for IT admin to manage