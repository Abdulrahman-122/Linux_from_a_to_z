# Device files;
  -to get to your device files;
    /dev on root directory
<img width="563" height="252" alt="image" src="https://github.com/user-attachments/assets/814f5ae3-ad3d-4d06-8fd1-7e9db8499319" />
the type of these files; 
  1-character devices as it starts with c as you see.
    -these devices are for data streaming (read,write)
    -kernal read , write on it
  2- Block devices;
    -programs on the system read from these files
    - sda..(disks) -> divided into blocks of data to be easy look for and find data in
  3. Pipe devices
    -like character one but it uses another process for read , write rather than kernal
  4. Socket device 
    - are used for interprocess communications
----

dd command
  - read,write contents from a device file and write into any file you want on your system
  - <img width="817" height="131" alt="image" src="https://github.com/user-attachments/assets/8cdc3585-9f79-45bb-863d-1a887f53ba5f" />

----
Hard Disks /dev/sd*;
  -these disks called on any linux by sda1,sdb1 ....
  - these disks are the partitions on the disks you made in order to efficient use of memory
  - also these small partitions called; scsi(small computer system interfaces)
  - also you can see your partitions on your linux version using this command;
    - lsscsi
      - <img width="727" height="93" alt="image" src="https://github.com/user-attachments/assets/78d0ce31-db03-4e0c-82d7-9247f98ed444" />
--------
Virtual Disksl; /dev/xvd*,/dev/vd*;
  -these are used for virtualization box like; virtual box,AWS machines.

----
Non-volatile memory devices;/dev/nvme*
  - some systems uses these disks to store in

------
Device mapper;/dev/dm* or /dev/mapper/
  - also may be used as storage type instead of nvme

-----
CD/DVD drives ; /dev/sr*
  -these are used to read from the disks 

----
PATA Hard disks; /dev/hd*
  - an older disks that are used for assignments
  - these maybe recognized as SATA disks

--------

Terminals ; /dev/tty, /dev/pts*
  - these are the software that attatched to the hardware of your device
  - there are ; dev/tty1 -> virtual terminal
  - /dev/pts0 -> first pseudoterminal
  - /dev/tty

- note;
  - your system depend on two modes; text mode,graphics mode
    - to switch between the modes
      - ctrl+alt+F1 -> convert from graphics-> text mode
      - Alt+f2 -> from text to graphics mode.
     
----
Audio Devices ; /dev/snd
  - sound devices that relay on ALSA(Advanced linux sound architecture)
  - these sound kernal devices are used while there are others that manage other sound devices , user devices.
- note;
  - you can make a device file on your system but this is danger
    - use , mknod command
      - mknod /dev/sda1 c 8 1 -> making device file as a  character type  it's major num is 8 , it's minor num is 1

--------------
Udevadm;
  - it's tool used to explore system devices and  monitor uenvent from the kernal.
  - to see  info about your disk
  - run this command;
  - <img width="1198" height="316" alt="image" src="https://github.com/user-attachments/assets/166b494b-a33b-4327-a392-28a6b79865aa" />
note; udevadm -> came from udev -> which  is the tool that responsible for manage devices,create it on the system....

  -to see the uevents of kernel;
    -<img width="1144" height="101" alt="image" src="https://github.com/user-attachments/assets/948661ca-9e48-4c04-b40e-dc42ea80a81d" />
  - to see the uevents of both udev,kernel
    - <img width="979" height="129" alt="image" src="https://github.com/user-attachments/assets/77a1e230-51ba-459d-9637-9bbbbc01d09c" />
-------
Here the linux SCSI subsystem actually look like:
  <img width="428" height="697" alt="image" src="https://github.com/user-attachments/assets/e09318c6-4834-48ba-a034-dace242d2073" />

  - you have three layers
    - block layer => /dev/sd* this is responsible for operation of class of devices.
    - SCSI subsystems -> this is responsible for traking scsi messages beteen bottom,top layer
      - manage bus drivers
    - bottom layer
      - hardare layer that manage SCSI in hardware drivers like;SATA,USB...
     note;
      -kernel  uses one driver at the top layer+uses another one driver at the bottom one for  a specific device
      - ex;
        if the device  was ;
         /dev/sda -> it uses    /sd at the top, /ATA at the  bottom one
- also to make communication between SCSI,USB system;
  -you need to ; USB storage driver=> translator between SCSI,USB ->  translates SCSI commands
- also to make communication from SCSI to harddisk -> we use
  - SATA driver in  order by using Libeta language to make translation between commands that are send to the harddisk from  the SCSI

- at the end of this chapter;
  - to access any device on your system
    - if you want to read from it -> use -> sr driver
    - if you want to write to it -> use sg driver
      - <img width="677" height="655" alt="image" src="https://github.com/user-attachments/assets/76a94edf-ae56-4267-8d09-de5ccae30468" />

To sum up:
  - I got from this  chapter;
    -   the  types of devices on my system  like; sd,nvme,cd,SATA,....
    -   shape of sd  device
    -   how  kernel uses sd  to send commands through  3 layers (block device,SCSI block,hardware block)
   
Alhamdullah on every thing
