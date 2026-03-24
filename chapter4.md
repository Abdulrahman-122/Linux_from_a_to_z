- Any Disk like;/dev/sda you have created (it's form look  like this)
    <img width="476" height="412" alt="image" src="https://github.com/user-attachments/assets/43fb6626-acee-4b32-be0a-baee60388fa3" />
  -The most important thing is : Partition table;
  - Types of Partition table:
    - MBR(msdos) ->master boot record partition table (older type)
    - GPT -> Globally partition table (newer one)
  - Some tools are used  to detect  and create disks on the system;
    - fdisk -l , parted -l
      - <img width="951" height="457" alt="image" src="https://github.com/user-attachments/assets/1b7813be-b8de-495f-99e3-66981d68d575" />

-----
What is  the contents MBR?
  - contain ; primary,extended(logical) partition types
    - primary contain 4 partitiions
    - if partition > 4 use extended then  broke it into logical paritions.
    - <img width="615" height="84" alt="image" src="https://github.com/user-attachments/assets/3ff5cff4-4a33-4468-a2be-8735d9dd9d29" />

------
After you altered your partition table or change it ;
  -use these commands to check;
    -///proc/partitions

-----
How to create a disk on your sytem?
  -first you need to know what types of disk devices  you use whether it sd* or  nvme* as  I use
  - <img width="963" height="271" alt="image" src="https://github.com/user-attachments/assets/25d6e6e7-1c04-4e86-a455-dca472e2f798" />
  - then now you can change one of them or create new one ;
    - <img width="946" height="829" alt="image" src="https://github.com/user-attachments/assets/9c17fb4d-3adf-4896-9cbf-58a25eb4596f" />
uncompleted yet  ????


----
Filesystems (after you create a disk -> you need to create a filesystem)
 The filesystem provides a structure to store and retrieve data. It manages three main things:

  Data Storage: It decides exactly which "blocks" on your physical drive hold your actual file data (like a .py script or a photo).

  Metadata: It stores information about the file: its name, when it was created, who is allowed to read it (permissions), and its size.

  Hierarchy: It creates the "tree" structure you see in Linux (starting from /), allowing you to put files into folders (directories).

2. Common Types (The "Languages")
  - btrfs(butter filesystem) -> modern filesytem that are used in linux distro like; arch,debian...
  - ext4(fourth extended filesystem) -> are the older one than btrfs
  - NTFS -> used in windows world
  - FAT,exFAT -> used in USB drives
  - APFS -> used in macos

notes;
  -creating a filesystem 
    -must be with a new disk
    -[warning] if  you made a new filesytem over an old one -> data of old one will be lost
    - this is if you want to see the filesystms files on your system;
    commands to create a filesystem;
      - to create a filesystem of ext4 type on a new disk ;mkfs -t ext4 /dev/sdf2 
      - then to mount that filesystem to the pc or your lap 
        -note;mount -> is to subject the filesystem to a directory in the system any directory
      how to mount ;
        - mount -t type device mountpoint
          ex;
          mount -t ext4 /dev/sdf2 /home/extra   -> this will mount the filesystem to directory extra in home
        - to unmount a filesystem;
          umount mountpoint 
          or 
          umount device_disk
        -  to  see info about mounting;
          - hit; 
              mount 
          - to see the blocks that  you created and subjected on points
            - use ; lsblk
    - if you want to mount a disk using a UUID(universal unique identifier )
      first; see the UUID for the new disk that you want to mount 
      as in this ex;
        <img width="651" height="167" alt="image" src="https://github.com/user-attachments/assets/191c9b19-208f-4ce7-957d-0e626eb6c1cb" />

  -  then do this ;
    -  mount UUID=b600fe63-d2e9-461c-a5cd-d3b373a5e1d2 /home/extra

- notes;
  - kernel read data from the cache  to ensure fast access
  - and cache read data from the RAM
  - if the data isn't in RAM -> RAM read from disk by creating a frames  into it and store data from disk to the RAM
 
  -you can specify more the mounting of your filesystem that you have creatd  by do these options
  mount -t vfat /dev/sde1 /dos -o ro,uid=1000
  -o ro -> create option mode with read only filesystem
   you can use;  -o rw => creating read write filesystem

   - you can see more  info about the filesystem from;///etc/fstab file;
       - you can see more info about filesystem by writing; df
         <img width="1583" height="447" alt="image" src="https://github.com/user-attachments/assets/509c4a01-aac6-487d-8742-1c45c693a2fe" />
       -  




    
