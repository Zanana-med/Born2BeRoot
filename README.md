<h1 align = "center">Born2BeRoot</h1>
<p align = "center">
		<img src = "https://i.ibb.co/jh9jq5f/image.png"  width = "250">
</p>

## How this article gonna help !


You wanna pass the 42 Born2BeRoot Project **DO YOU ??** 

So we're going into the main PDF subject, and everytime we find a keyword or any scary word that we don't face everyday ! We gonna take our time to understand it and know how to work with it. Part per Part of the PDF until we finish the whole project ✅

<br>
# <u>Let's start !</u>

![introduction](https://i.ibb.co/K0sDzJQ/image.png)


>Machine ?????

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

You think that Linux is an entire operating system where you run commands like `ls`, `cp`, `cat`, etc. Including shell command-lines and libraries such glibc for running prorams.

But you're completely wrong my friend! Because here you are talking about the GNU not the Linux.

Linux is the kernel, the core of the operating system, the entire OS is named GNU/Linux which combine the Linux kernel and the GNU Project tools and utilities

<p align = "center">
	<img src = "https://i.ibb.co/3SGWjhB/9bygum.jpg" width = "250">
</p>


Before diving into the Debian, Rocky and the difference between them, we need to understand those two concepts :

### > Linux distribution : 
 
Linux distribution is a complete operating system built around Linux kernel with additional software like system libraries, utilities and package management tools, created from groups and individual developers for specific purposes.  

### > Package manager : 

Command-line or graphical tool to automate the process of installing, updating and removing software packages on Linux system, don't be scared by the word **package** you can see it as a normal software you wanna install, to install our package we need a package manager 