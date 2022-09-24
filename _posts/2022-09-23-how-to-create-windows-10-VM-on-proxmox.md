---
author:
  name: Paulo Henrique Zanoteli Santos
title: How to create windows 10 VM on Proxmox
date: 2022-09-23 21:00:00 UTC-3
categories: [Guides, Proxmox]
tags: [install-guide, config-guide, virtualization, proxmox]
---

## 1 - Get windows 10 and Virtio-drivers ISO's

[Windows 10](https://www.microsoft.com/pt-br/software-download/windows10)

[Virtio drivers stable](https://fedorapeople.org/groups/virt/virtio-win/direct-downloads/stable-virtio/virtio-win.iso)

## 2 - Upload your ISO's to proxmox server

1 - First, click on **local**, go to **ISO Images**, after click on **upload**:

![Upload 1](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/1.png)

2 - Now chose your **ISO**, and click on **upload** (**WAIT FOR 100%**):

![Upload 2](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/2.png)

\* You can change file name if you want to

## 3 - Create VM

1 - Now, let's create the VM (virtual machine), First, click on **Create VM (Up right)**:

![Create VM 1](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/3.png)

2 - Choose a **name** for your VM:

![Create VM 2](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/4.png)

3 - Choose your windows 10 **ISO**, and change **Type** to **Microsoft Windows** and **version** to **10/2016/2019**, gonna be like this:

![Create VM 3](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/5.png)

4 - Check **Qemu Agent** box: 

![Create VM 4](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/6.png)

5 - Change **Bus/Device** to **SCSI**, **Cache** to **Write back**, You can choose your **Storage** and **Disk size** (You can change **disk size** later):

![Create VM 5](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/7.png)

6 - Select how many **cores** and **sockets** you want (You can change it later):

![Create VM 6](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/8.png)

7 - Select how much **memory** you gonna give it (You can change it later):

![Create VM 7](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/9.png)

8 - Change **model** to **VirtIO (paravirtualized)** and **disable firewall** (You can change it later):

![Create VM 8](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/10.png)

9 - Now, check everything and after click on **finish** and wait for the VM be created:

![Create VM 9](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/11.png)

## 4 - Windows installation

1 - First, we're going to add our virtual drivers to installation, click on your VM, go to **hardware section** and click on **Add**, click on **CD/DVD Drive**:

![Windows installation 1](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/12.png)

2 - Select your **virtio drivers**, change **ID number** to **1** and click on **Add**, probably is gonna be like this:

![Windows installation 2](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/13.png)

3 - If everything's correct, your **hardware section** has to be similar to this:

![Windows installation 3](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/14.png)

4 - Go to **Console section** and click on **Start Now**:

![Windows installation 4](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/15.png)

5 - Now, proceed with windows installation till you get to "Which type of installation do you want?", Select **Install windows (advanced)**:

![Windows installation 5](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/16.png)

6 - As you can see, there's no disk. So we have to load the drivers:

![Windows installation 6](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/17.png)

7 - **Browse**:

![Windows installation 7](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/18.png)

8 - Select the **CD driver** that we loaded in **step 2**:

![Windows installation 8](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/19.png)

9 - Select **vioscsi**, **amd64** and click ok:

![Windows installation 9](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/20.png)

10 - Click **next**:

![Windows installation 10](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/21.png)

11 - Now, as you can see, our disk is loaded (I added more 28GB):

![Windows installation 11](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/22.png)

12 - Now do the same to **NetKvm**:

![Windows installation 12](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/23.png)

13 - And the same to **Balloon**:

![Windows installation 13](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/24.png)

14 - proceed with windows installation till get to desktop.

## 5 - Desktop configuration

1 - First, right click on **windows logo** and click on **Device manager**:

![Windows configuration 1](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/25.png)

2 - As you can see, we've to install some drivers, double left click on **PCI Simple Communi...**:

![Windows configuration 2](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/26.png)

3 - Click on **Update Driver**:

![Windows configuration 3](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/27.png)

4 - Select **Browse my computer for driver software**

![Windows configuration 4](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/28.png)

5 - Click on **CD/DVD Drive** with **virtio drivers**: 

![Windows configuration 5](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/29.png)

6 - Click **Next**:

![Windows configuration 6](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/30.png)

7 - Click **Install**:

![Windows configuration 7](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/31.png)

8 - As you can see, everything is installed:

![Windows configuration 8](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/32.png)

9 - Open **windows explorer**, go to **This PC**, go to **CD Drive** with **virtio drivers**:

![Windows configuration 9](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/33.png)

10 - Open **guest-agent**:

![Windows configuration 10](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/34.png)

11 - Install **qemu-ga-x86_64**:

![Windows configuration 11](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/35.png)

12 - Now that everything's installed, **shutdown** the machine, go to **hardware section** and remove **Windows ISO** and **Virtio drivers**:

![Windows configuration 12](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/36.png)
![Windows configuration 13](/assets/img/posts/2022-09-23-how-to-create-windows-10-VM-on-proxmox/37.png)

## Documentation and Utilities

[Proxmox offical documentation](https://pve.proxmox.com/pve-docs/)

[Tutorial video](https://www.youtube.com/watch?v=6c-6xBkD2J4&ab_channel=TechnoTim)
