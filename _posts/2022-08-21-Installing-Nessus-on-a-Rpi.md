---
layout: post
title: Installing Nessus on a raspberry pi 4 
subtitle: A step by step guide to install Nessus on a raspberry pi 4
thumbnail-img: /assets/img/rbpi/rbpi.jpg
tags: [Raspberry-pi, Tech, Nessus, Vulnerability Management, Security]
---


## Installing Nessus on a raspberry pi 4

Usage: Someone may ask, till now people were installing Nessus on a virtual machine or a server and it works fine. Then why on a raspberry pi. The simple answer is that we can carry this cheap kit to anywhere and can run in a network and nobody can notice it physically. For sure a network administrator has all the privileges to find if a raspberry pi is running in the network.

Hence tenable has released a Nessus package for ARM CPU which is there on the Raspberry pi.

## Pre-requisite

TLDR; Raspberry pi with 32 bit raspberry pi OS installed. 

The only pre-requisite for this installation is a raspberry pi kit with Raspberry pi 32 bit OS installed. While writing this blog tenable has released a 32 bit Nessus package only. So incase if you are trying to install it on a 64 bit package you may face some problem as I have gone through the same. But it should not be the case. As far as I know all the 32 bit software should support on 64 bit CPU. If you know why that is happening please let me know. 

## Installation

/assets/img/rbpi/

Without any further delay, let’s see what all steps someone should follow to do it. The best place to get started is the tenable [documentation](https://docs.tenable.com/nessus/Content/InstallNessusRaspberryPi.htm) itself. 

![tenable.png](/assets/img/nessus-rbpi/tenable.png)

From here we can download the required Nessus package after agreeing the terms and conditions.

![Untitled](/assets/img/nessus-rbpi/Untitled.png)

Once downloaded we can use the below commands to install the Nessus.

```bash
cd Downloads/
sudo dpkg -i Nessus-10.3.0-raspberrypios-armhf.deb
sudo /bin/systemctl start nessusd.service
```

![nessus installation.png](/assets/img/nessus-rbpi/nessus_installation.png)

Now open the browser on raspberry pi and go to [https://raspberrypi:8834](https://raspberrypi:8834). Congratulations Nessus installation is successful if you see a certificate error on the browser. 

![first-webpage.png](/assets/img/nessus-rbpi/first-webpage.png)

 Now select the Nessus essentials. If you have a license for others you can go with that.

![3rd-webpage.png](/assets/img/nessus-rbpi/3rd-webpage.png)

 In the next screen fill the details and click on “Email”

![4-webpage.png](/assets/img/nessus-rbpi/4-webpage.png)

 You will receive and activation code on your mail address and fill that in the next page.

![5-webpage.png](/assets/img/nessus-rbpi/5-webpage.png)

You will be asked to setup the username and password for signing up. Once that is done you can sign in to Nessus console.

![Untitled](/assets/img/nessus-rbpi/Untitled%201.png)

It will take a lot of time to download and compile the plugins, which are the core things used during a vulnerability scanning. 

![2nd-webpage.png](/assets/img/nessus-rbpi/2nd-webpage.png)

After logging in we can create a scan as per our requirement. Creating a scan is very easy on Tenable. 

Click on **New scan**

![Untitled](/assets/img/nessus-rbpi/Untitled%202.png)

Select the scan template. Here we will select the “Basic Network scan”

![Untitled](/assets/img/nessus-rbpi/Untitled%203.png)

Now fill the details in the form → Name, Description, Targets. Then click on the small drop down button near to save button and click Launch,

![Untitled](/assets/img/nessus-rbpi/Untitled%204.png)

Now we can see a scan has been started.

![Untitled](/assets/img/nessus-rbpi/Untitled%205.png)

After some time the scan will be completed and we can see the results.

![Untitled](/assets/img/nessus-rbpi/Untitled%206.png)

![Untitled](/assets/img/nessus-rbpi/Untitled%207.png)

Next we can export the report or we can do the analysis of the vulnerabilities. 

That’s all for this blog. If you want to get a brief idea about the Vulnerability assessment, then you can check my `Vulnerability assessment` blog.  Thanks for reading and please reach out to me for any feedbacks.