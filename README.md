<h1 align = "center">Born2BeRoot</h1>
<p align = "center">
		<img src = "https://i.ibb.co/jh9jq5f/image.png"  width = "250">
</p>

## How this article gonna help !


>**WE ARE NOT HERE ONLY FOR THE CONFIGURATION OF THE VIRTUAL MACHINE, IF THAT'S WHAT YOU WANT DON'T CONTINUE THIS MASTERPIECE ARTICLE WHICH FULL OF KNOWLEDGE AND INFORMATION, GO WATCH A 10 MIN YOUTUBE VIDEO AND STAY LIKE AN ILLITERATE** 

You wanna pass the 42 Born2BeRoot Project **DO YOU ??** 

So we're going into the main PDF subject, and everytime we find a keyword or any scary word that we don't face everyday ! We gonna take our time to understand it and know how to work with it. Part per Part of the PDF until we finish the whole project ✅

<br>

# <u>Let's start !</u>

![introduction](https://i.ibb.co/K0sDzJQ/image.png)


**Machine ?????**

The `Machine`here refer to the **Virtual machine** exactly. Let's understand what is it, and why you should use one also ! ...

# **Virtual Machine**

So basically you can see a VM as a computer inside your computer.

Imagine you have a computer with Windows operating system, one day you decide to start learning Linux! But you still wanna use your main computer which full of your personal data and software you use everyday .  

Of course you need to practice not just wasting your time by just watching YouTube playlists or even paid courses.  

So now you should buy a new laptop so you can install the Linux operating system and start practice your knowledge.  
**Isn't that just waste of your goddamn MONEY ??**  

VM is here to help you !

A Virtual Machine allows you to run an **entire** operating system inside your current system, isn't that great.

![VM](https://i.ibb.co/Kj5z1n6/image.png)

### **Host & Guest**  

+ The **HOST** is the operating system with the physical connection with your hardware (in our example its your Windows which contain your files, data, software, etc.)    
+ The **Guest** is the new operating system you run inside the virtual machine (In our example its the Linux so you can practice your knowledge).

The guest also use the resources of the computer (CPU, RAM, Storage, etc.), not directly of course! but with the help of the **Hypervisor**.  

# **Hypervisor**

The hypervisor is just a software installed in your host OS, its job to create computers inside your computer (VirtualBox for example).  

The hypervisor create for every new OS all the resources it needs so the new VM thinks that's it is actually a computer.

<p align = "center">
	<img src = "https://i.ibb.co/hRRf3Fz/Hardwar-1.png" width = "550">
</p>

The Hypervisor manage and allocate the portions of all the resources needed so that every OS think its inside a real computer.

+ **Virtual CPU :** The hypervisor allocate certain number of vCPU (Virtual CPU) to the virtual machine, which are abstracted from the physical CPU.

+ **Virtual Ram :** When configuring a VM, you choose how much the hypervisor allocate of the physical memory to the guest OS from the host RAM, ensuring it wouldn't access the other host memory.

+ **Virtual storage :** Hypervisor provide the number you want of GB as the guest hard disk from the host hard one, it create a large file on the host storage, this file act like its the Virtual storage of the guest OS.  (  `.vdi` file on VirtualBox).

+ **Virtualizing other resources :** the hypervisor also provide the other virtual resources as Gpu, Network adapter, Usb devices ... 

### Types of Hypervisor :

1. **Type 1 :** ( Bare Metal Hypervisor) This type don't need an interaction with a host operating system, requires setup knowledge. It take all the resources it needs directly from the physical hardware, it is used mostly by the companies, servers, cloud computing ...  And not for personal uses or testing a new OS.

2. **Type 2 :** ( Hosted Hypervisor ) This type of hypervisor is the one we gonna use on our project, it is easy to set up and great for personal uses or testing, it runs on top of a host OS as an application.

<p align = "center">
	<img  src = "https://i.ibb.co/R90SPtL/Untitled-design-1-1.png" width = "600">
</p>

# **Operating System, Linux, Debian and Rocky**

![Os & Debian](https://i.ibb.co/ZY1Qdmx/image.png)

### > Operating System

The operating system is a software developed using programming languages like C, C++ or Assembly. It act like intermediary between the user and the computer's hardware, manage the hardware resources as CPU, RAM, Storage, Peripheral ( keyboards, mouses, usb's etc. ),  run applications and provide user interface for the interaction.

The operating system interact directly with the hardware with the help of its kernel and device drivers.

**Kernel :** The core part of the operating system that interact directly with the hardware, acts as a bridge between the hardware and the rest of the operating system, enabling communication between the software and the hardware.  

>**How to communicate with the kernel ?**

<u><b>System calls</b></u> : Are the primary interface between the user programs and the kernel, allow user applications to request services from the operating system such file access, process control or communication ... 

<p align = "center">
	<img src ="https://i.ibb.co/DVdJDbN/User-space-2.png" width = "450">
</p>


### > Linux is not what you think it is !!!!!

You think that Linux is an entire operating system where you run commands like `ls`, `cp`, `cat`, etc. Including shell command-lines and libraries such glibc for running programs.

But you're completely wrong my friend! Because here you are talking about the GNU not the Linux.

Linux is the kernel, the core of the operating system, the entire OS is named GNU/Linux which combine the Linux kernel and the GNU Project tools and utilities

<p align = "center">
	<img src = "https://i.ibb.co/3SGWjhB/9bygum.jpg" width = "250">
</p>


Before diving into the Debian, Rocky and the difference between them, we need to understand those two concepts :

1. **Linux distribution :**
 
Linux distribution is a complete operating system built around Linux kernel with additional software like system libraries, utilities and package management tools, created from groups and individual developers for specific purposes.  

2. **Package manager :** 

Command-line or graphical tool to automate the process of installing, updating and removing software packages on Linux system, don't be scared by the word **package** you can see it as a normal software you wanna install, to install our package we need a package manager.

>On the next chapter we gonna give more time to APT and explain the package manager and how it works .


### > Debian and Rocky

+ **Debian** is a Linux distribution composed of **free** and open-source packages, comes with clean user interface not like the Windows OS fooled of news and ads, its update are well tested before releasing. The Debian distributions focus more on the stability, security and privacy of the user, also comes with the powerful package manager APT which help a lot for installing, upgrading or removing software on the system.

+ **Rocky** is based on Red Hat Enterprise Linux (RHEL), which is a Linux distribution for the commercial market developed by the Red Hat, Rocky focus on enterprise-grade software. Good for servers, enterprise environment, cloud computing ... Not for a beginner with the Linux operating system.

#### Why Debian ?

I think we already answer that from explaining each one of  them, Rocky is for the enterprises and companies not for someone new to learn system administration and basic Linux concepts, also Debian has more packages.


# APT, Aptitude and AppArmor


![apt](https://i.ibb.co/Rcmh9mV/image.png)


### > Package Manager

We talk earlier about the package manager, now its the time to go deeper.

As we say that the package manager can be a command-line or a graphical tool help us to install, upgrade and remove packages which are software .

`dpkg` is one of the package managers, but i don't recommend it for you, because you're going to face a lot of problems, first you need to find and download the `.deb` file of the package you wanna install, but the big problem is when you face the  **dependency** problem. 

**What is dependency ???**

When installing a package it depends to other packages to work, using **dpkg** you need to install them manually if they not exist on your system. Instead! there is other package managers that install the dependencies automatically like **APT** the powerful package manager.

![dependency Problem](https://i.ibb.co/fqkQ22f/2-dependency-error-teamview-2.png)


### > APT

**APT** stand for Advanced Package Tool, released on 2014, a powerful package manager used by Debian-based Linux Distributions ( Ubuntu, Linux Mint, etc.). It simplifies the process to manage packages by automating tasks as resolving the dependencies and downloading packages from repositories.  

Unlike `dpkg` you don't need to install the `.deb` file, just use the apt command plus the name of the software you wanna install. THAT'S IT !


example : `apt install firefox`


The APT automatically install and update all the dependencies needed to install a package.

**Apt and Apt-Get :** The both apt and apt-get access the same back-end resources, we're talking about the same repositories for downloading and managing software packages.
Apt is newer than Apt-Get, also the Apt is user-friendly interface and provide cleaner output and progress bars for a better user experience.

<p align = "center">
	<img src = "https://i.ibb.co/3SrxBfs/Linux-Users-960-x-1100-px-960-x-1000-px-1-1.png" width = "350">
</p>

**How APT works ?**

Apt relied on a list of repositories which are storage location or someone's server with collection of software, we can check those repositories using the command `/etc/apt/sources.list` and for additional files in `/etc/apt/sources.list.d/`.

When requesting a package \` `apt install firefox` \`  the Apt checks which dependencies are needed to install the package and ensuring installing them if they not exist, then tha Apt download the `.deb` package file from the repository specified in `source.list`.


**Update Package Metadata**

When you run : `sudo apt update` the Apt downloads the latest updates of the packages from the repositories as versions, dependencies and descriptions and store this data locally on `/var/lib/apt/lists/` for faster lookups.  


### > Aptitude

The aptitude is a package manager older than the APT, it was released on 1999. It offers additionally of the command-line interface a **full-screen text-based graphical interface**,  making it more user friendly, also it shares the same back-end resources as APT.

(Snapshot of the Aptitude graphical Interface)
![Aptitude](https://i.ibb.co/DttnPPK/image.png)



**So why APT created?**

`apt` and `aptitude` are **complementary**, not competitors. The APT was not created to kill the Aptitude or something like that, the APT focus on modernization, before APT the package management required using multiple tools like `apt-get` , `apt-cache` , `dpkg` , etc. The APT merge all those functionalities into a single. 

For example :  
+ Old way : `apt-get install`, `apt-cache search`.
+ New way : `apt install`, `apt search`.  


### > AppArmor

AppArmor is a Linux Kernel security module restrict the resources that the program or application can access, enhancing the system's overall security.

 **-** Check if active : `systemctl status apparmor`

**Example :**  Web-Browser don't need to access system files like `/etc/passwd` or your private data as photos. AppArmor restrict the browser to access those directories and files, so even if the program is hacked, the hacker will not have the access to sensitive data.

The AppArmor uses set of rules called **profiles**, which is a configuration file that contain :
+ what files a program can access to ;
+ what system resources can be used (Webcam as example, etc.) ;
+ what types of actions a program can take (connect to internet but not run other programs) .

AppArmor links a profile to a program by matching the profile's **name** to the application **executable path**. 
+ Path of Firefox ---> `/urs/bin/firefox`
+ Firefox Profile name ---> `/etc/apparmor.d/usr.bin.firefox`

**Example of a Profile file:**

![Profile Example](https://i.ibb.co/q9KWmZn/Croped-Profile-example.png)


AppArmor can use two modes to handle profiles :
+ **Enforce mode** : The profile is active and the AppArmor block actions not allowed by the profile. To set ---> `sudo aa-enforce /etc/apparmor.d/usr.bin.firefox`
+ **Complain mode** : The profile is active but the AppArmor just logs violations without blocking them, this mode is good while testing a profile. The logs are on the default Linux logs path `/var/log/syslog` . To set ---> `sudo aa-complain /etc/apparmor.d/usr.bin.firefox`

**Loading a Profile :** When creating or updating a profile we need to load this file to AppArmor so when enforcing it the system knows what to enforce.  
The command is  ---> `sudo apparmor_parser -r /etc/apparmor.d/usr.bin.firefox` 


# Filesystem, Partitioning, LVM and Mounting

![Partitions, LVM](https://i.ibb.co/C5z346x/Lvm-Partitions.png)

## > Linux File System

> **NOTE THAT EVERYTHING IN LINUX IS A *FILE* !!!**

![Linux--File-System](https://i.ibb.co/6nSLhsJ/New-file-system-picture.png)

The Linux file system is a structured way to organize and manage data on device in Linux OS. Let's give some time to the important directories on the root directory tree.

+  `/` : Root directory the top-level directory on Linux, if something happened to root directory that can cause to the entire system fail .
+ `/home` : Store personal data and configurations for each user .
+ `/boot` : Contain files needed for the system to boot .
+ `/bin` (essential binaries) : Contain the basic commands as `ls`, `cat`,`cp` in machine code .
+ `/sbin` : System binaries, includes the super-user commands used for system administration  like `adduser`, `userdel` ...
+ `/lib` : Houses essential shared libraries required by the `bin` and `sbin` binaries .
+ `/etc` : Human editable files for the system-wide configuration like `network`, `bluetooth`, `passwd` for the users account information ...
+ `/tmp` : Temporary storage for files used by programs during runtime, all those files are clearer after reboot.

## > Partitions
The partitions on the Host are a division of the device storage (HDD, SSD) into separate, isolated sections.

For Guest the entire virtual partitions located inside the file allocated by the hypervisor as the virtual hard disk,  Each section act as a separate **container** for a specific purpose (OS files, user data, swap space, etc.).

**Types of Partitions :**

+ **Primary Partitions :** Is a directly accessible section of the disk that can store data or an operating system, every VM at least use one primary partition for the **root** filesystem .
+ **Extended Partitions :** Are container partition that holds additional partitions called logical partitions .
+ **Logical Partitions :** Exist inside an extended partition and behave like primary partitions, they are  numbered starting from `5` (`/dev/sda5` , `/dev/sda6` ...). Logical partitions are ideal for organizing data (separating `/home` and `/var`)
<p align = "center">
	<img src = "https://i.ibb.co/m8H02qx/MBR-Croped.png" width = "500">
</p>

## > LVM 

 [The Best YouTube Video To Understand The Configuration of a LVM Using Terminal](https://www.youtube.com/watch?v=214rUhQe7B4&t=98s&ab_channel=DorianDotSlash)

LVM is short of Logical Volume Manager, allow the creation of **Groups** of disks or partitions that can be assembled into a single (or multiple) filesystems.  
Can be used nearly for every mount point **EXCEPT** `/boot`, because GRUB cannot read from LVM metadata.

With LVM you can resize the volumes however you want, you can shrink the volume for the unused space, also growing the volume if you face the `space remaining` Linux message or just if you need to.  

>DON'T LET THIS PICTURE SCARE YOU BODY! BY THE END OF THIS CHAPTER YOU GONNA UNDERSTAND EVERYTHING I PROMISE.

![LVM](https://i.ibb.co/bgkZVyR/image.png)

So this picture provide us how the LVM is structured on the Linux system :

- **Hard Drives :** Are the physical disks installed on the system (HDD, SSD, also USB it can plays as a hard drive). They are represented from `/dev/sda` for the first hard drive, `/dev/sdb` for the second and so on.

- **Partitions :** We may only need a single part of the drive for the LVM, so we divide the drive into two partitions (`/dev/sda1` for LVM, and `/dev/sda2` for `/boot` for the system bootloader or the `/swap` partition)

  >**THE LVM STRUCTURE START FROM HERE**
  
- **Physical Volumes :** Is a partition (or an entire disk) crated using `pvcreate` command prepared to be used by LVM, After using the command `pvcreate` the partition recognized as a Physical Volume, and we cannot name the PV for example now the `/dev/sda1` is a Physical Volume we cannot rename it to `pv1`, also we can't combine two partitions into one single PV even if they are on the same disk. Each PV must map to a single partition.
  
- **Volume Group :** The one responsible to combine multiple Physical Volumes into a single logical storage pool using the `vgcreate` command, the size of the VG is the sum of the PV, we can name the VG as we want, `vgcreate datavg /dev/sda1 /dev/sdb1 ...` we create a VG named `datavg` combine all the Physical Volumes in one space. 
  
- **Logical Volumes :** Are created by allocating space from the VG using the `lvcreate` command, LV are virtual storage area and the function like partition  but more flexible because we can play with its size the way we want
## > Mounting
Mounting refers to the process of making a `storage device` or a `filesystem` accessible and attached at a certain point in the directory tree called a mount point.

If you have a USB drive at `dev/sdb1` and you want to mount it to the `/media/usb` directory you have yo use the command `mount /dev/sdb1 /media/usb` 

For example you plug-in the USB and you don't mount it to a filesystem you won't be able to access to the files on the USB, because Linux needs the filesystem to be integrated into the directory tree.