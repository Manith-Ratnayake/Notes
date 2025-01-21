A device driver (driver) is a piece of software that controls a particular type of device which is connected to the computer systems

Device driver has 3 sides
    - One side talks to the rest of the kernal
    - One talks to the hardware
    - One talks to the user


   User ------------------
    |                    |
    |                    |
    |                    |
   Kernal                |
    |                    |Device file
    | Device Driver      |
    |                    |   
   Hardware ------------ |


What is kernal module 
- Traditional way of adding code to the kernal was to recompile the kernal and reboot the system
- Kernal modules are piece of code that can be loaded/inserted and unloaded/removed from the kernal as per the dameon need

Other Name
    1. Loadable Kernal Module (LKM)
    2. Modules

Extenion .ko (kernal object)
Modules are installed on the lib/modules/< kernal version> 
