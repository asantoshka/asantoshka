---
layout: post
title: Setting up a Raspberry pi 
subtitle: A step by step guide to setting up raspberry pi
thumbnail-img: /assets/img/rbpi/rbpi.jpg
tags: [Raspberry-pi, Tech]
---

# Setting up a Raspberry pi


This blog includes a step by step guide to install and start a raspberry pi. We will see how to assemble a raspberry pi kit, connecting various cables and installing raspberry pi OS.

🙏🏻 I have received this raspberry pi kit from team tenable after a small quiz. A huge thanks to [Tenable](https://www.tenable.com/campaigns/nessus-on-raspberrypi).



## Components used:

1. Micro SD card
2. Raspberry pi 4 8 GB
3. 3A USB-C power adapter
4. USB Micro SD card reader
5. Micro HDMI cable
6. Monitor, Keyboard and Mouse
7. Case to hold/protect the Raspberry pi [Optional]
8. Cooling Fan [Optional]

![IMG_20220725_191343.jpg](/assets/img/rbpi/IMG_20220725_191343.jpg)

## Let’s get started..!!

### Assembling the kit

The first step to get started with this process is to know and assemble the kit we have. It’s really easy to do so. 

While assembling we need to start with raspberry pi module clipping it on the base of the case. The putting the middle portion of the case carefully. 

Then attaching the cooling fan on the top cover. After that we need to attach cooling fan cable to the the pins for power supply and attach the top cover on the kit now.  

![IMG_20220725_192106.jpg](/assets/img/rbpi/IMG_20220725_192106.jpg)

While connecting pins we can refer the below images.

![Fan](/assets/img/rbpi/fan.jpg)


As our hardware assembling is done we can now proceed for the installing OS and connecting the cables.

### Installing Raspberry OS

To get started with the OS installation we can install the [raspberry pi imager](https://downloads.raspberrypi.org/imager/imager_latest.exe) on our personal computer. 

Step 1: Open Raspberry Pi Imager

![Untitled](/assets/img/rbpi/Untitled%202.png)

Step 2: Click on **Choose OS** & select the required OS

![Untitled](/assets/img/rbpi/Untitled%203.png)

Step 3: Select Choose storage 

![Untitled](/assets/img/rbpi/Untitled%204.png)

Step 4: Click on write

![Untitled](/assets/img/rbpi/Untitled 05.png)

Step 5: Click on **Yes**

![Untitled](/assets/img/rbpi/Untitled%206.png)

Step 6: OS will be wrtiiten to the SD card now.

![Untitled](/assets/img/rbpi/Untitled%207.png)

Step 6: Click continue. Remove the SD card from PC. 

![Untitled](/assets/img/rbpi/Untitled%208.png)

Step 7: Insert into the raspberry pi.

![IMG_20220725_200523.jpg](/assets/img/rbpi/IMG_20220725_200523.jpg)

Step 8: Now connect all the cables to raspberry pi. (HDMI, Power supply, Mouse and Keyboard)

![IMG_20220726_120203.jpg](/assets/img/rbpi/IMG_20220726_120203.jpg)

Now raspberry pi should boot. Like any other OS, it will ask to select the keyboard layout, Language and Country from which it is going to be used. 

Once that is done it will ask to setup the wi-fi which is optional if the internet connection is going to be provided by an ethernet cable.

Next it will ask for the updates which can be ignored and can be updated using below commands.

 

```bash
sudo apt-get update
sudo apt-get upgrade -y
```

After proceed further we are all set with the raspberry pi. Congratulations!!

![Untitled](/assets/img/rbpi/Untitled%209.png)

Now one would like to install open-ssh on the host, so that it would be easier to connect to host from any other personal computer.

```bash
sudo apt-get install openssh-server
sudo systemctl enable ssh 
sudo systemctl start ssh
```

 Also we can set up the RDP on the raspberry pi using the below commands 

```bash
sudo apt-get install xrdp
sudo systemctl enable xrdp
sudo systemctl start xrdp
```

Thanks for reading till end of the article. 