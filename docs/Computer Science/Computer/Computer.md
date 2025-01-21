
Numbers
• Natural Numbers
Zero and any numbers obtained by repeatedly adding 1 to it
Eg: 45875, 0, 1254, 12
• Negative numbers
A value less than 0, with a ‘-’sign
Eg: -4581, -45, -1, -8
• Integers
Either a natural number or a negative number
Eg: 4587, 5, 0, -4, -4543
• Rational Number
An integer or a quotient of two integers
Eg: 458, 0, -754, 8/25, -2/5

Computer contain only 2 states
• low-voltage
• high-voltage


Why use Hexadecimal?
• More efficient to store large numbers
• Quick conversion between binary
------------------------------------------
Data Storage
Bit
• Binary Digit
• 0 or 1 → smallest unit
Nibble
• 4 bits → 1 Hex
Byte
• 8 bits
• Smallest addressable unit in computer
American Standard Code for Information Interchange
Data compression refers to any technique that recodes the data in a
file so that it contains fewer bits.
Compression techniques divided into two categories:
lossless and lossy
Lossless compression provides a way to compress data and
reconstitute it into its original state;
uncompressed data stays exactly the same as the original data
Lossy compression throws away some of the original data during the
compression process; uncompressed data is not exactly the same as
the original

The von Numann architecture
Arithmetic/logic unit
• Capable of performing arithmetic and logic operation
Memory Unit
• Holds data and instruction (holds the running program)
Input unit
• moves the data from outside world into the computer
Output unit
• Moves the data from inside the computer to the outside world
Control Unit
• manages all other component in the computer

System Interconnection
CPU connected to other components using buses (copper wire connections)
Address bus
• used by CPU to select which memory location or I/O or storage device to access
Data bus
• transmits binary data to or from CPU
Control bus
• used to control operation of memory (e.g. enable read or write control)
Modern Computers now use separate buses for more specific needs and to increase the speed of the system

RAM and ROM
RAM (random-access memory)
• memory can be accessed as well as changed
• volatile
• used as the working memory
ROM (read-only memory)
• can access the memory but not changed
• non-volatile
• used to store BIOS program
Secondary storage devices
• RAM is volatile
• Need a way to store the information
• The memory used to store the data
Eg:
magnetic tape
magnetic disk
optic disk
flash memory
--------------------------------------------------------------
Little Endian - Little-endian is an order in which the “little end"
(least significant value in the sequence) is stored first.
• Ex: 10 7D 00 stored as 00 7D 10
• Big Endian - Big-endian is an order in which the "big end" (most
significant value in the sequence) is stored first
• Ex: 10 7D 00 stored as 10 7D 00
------------------------------------------------------------------

IP Addressing
25-Nov-20 Module Code ModuleName 2
• An IP address is a numeric identifier assigned to each machine on an
IP network.
• It designates the specific location of a device on the network.
• IP addressing was designed to allow hosts on one network to
communicate with a host on a different network regardless of the
type of LANs the hosts are participating in.

Subnetting Basics
• Benefits of subnetting include:
• Reduced network traffic
• Optimized network performance
• Simplified management
• Facilitated spanning of large geographical distances.

The broadcast address is all host bits turned on, which is the number
immediately preceding the next subnet

Valid hosts are the number between the subnets, omitting all 0s and
all 1s.
-----------------------------------------------
A system → Software + Hardware
Software → System Software + Application Software
Operating System (OS) -> A System Software
What is an Operating System
Program that act as a interface between the hardware and the user 

How the OS is loaded
On pressing ‘Power Button’ on a computer
• Perform a POST (Power-On Self Test)
• Read the BIOS (Basic Input Output System)- ROM
• Read Disk Sector Zero
• Read partition Boot Sector
• Loads the OS (OS starts)
Functions of Operating System
• Process Management
• Memory Management
• Disk management
• File Management
• Security
• Control over system performance
• Error detecting aids
• Coordination between other software and users

What is computer memory
20/10/2020 CM1604 Computer Systems Fundamentals 14
Where the instruction and information about current active
process are being stored
- Working memory of CPU
- Transient
● OS should have techniques to keep track of / manage how the
memory is utilized
Memory Management

Memory Management
• Allocate memory for process when needed
• Deallocate when no longer needed
• Keep track of the areas of memory which as used
• Enable memory sharing between processes
• Protect the memory allocation of a process from another
• Manage memory swapping between the memory and secondary
storage
• Conversion of logical address into physical address

Memory is a continuous set of bits
referenced by specific addresses
Logical Address:
Location in the memory relative
to the program
Physical Address:
Actual address in the main
memory
Single Contigious MM
• Apart from the Operating System,
only one application will be in the
memory
• Simplest form of memory
management
