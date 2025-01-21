What is Kerberos?

A protocol used for authentication
Uses tickets to authenticate and identify
Uses symmetric key crypto


Active directory uses Kerberos by default
Passwords are not stored on the local workstation any longer : stored on domain controller



1. Clients sends TGT
2. KDC verifies the credentials and sends back the encrypted TGT
3. Client stores TGT locally
4. Client sends local TGT with SPN for the service it want to access
5. TGS sends session key for the service to Client
6. Client sends session key to service



What is a Kerberos realm?

Admin created 
Contains all machine available for access
Policy restrictions
The client, 



Contains 2 section
1) KDC Clients - Workstation, HTTP service, Email service, File sharing service
2) KDC itself - authentication server, Ticket granting server


Request a TGT 
* Client sends plaintext Request for a TGT
-- Name
-- Name of service
-- IP address
-- Lifetime of ticket 




All applications ran use memory, this includes operating systems

When an appilication loads it will load itself into memory
When this happens EIP will start moving through the code based on its entry points and start executing the instructions at each memory level

What we have talked about so far is physical memory there is such thing as virtual memory, this is often called SWAP

Swap loads bits of memory phycially on the hard drive that is not as commonly used to conserve space in RAM 
This makes reading from SWAP much slower than RAM but will allow you to store more data in memory