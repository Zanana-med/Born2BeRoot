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

## **Virtual Machine**

So basically you can see a VM as a computer inside your computer.

Imagine you have a computer with Windows operating system, one day you decide to start learning Linux! But you still wanna use your main computer which full of your personal data and softwares you use everyday .  

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

### **Hypervisor**

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

