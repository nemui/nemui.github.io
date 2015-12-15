---
layout: post
title:  "USBNetwork and Extend"
date:   2015-12-15 11:14:18 +0900
categories: kindleberrypi kindle ssh raspberrypi
---
Last time [we performed a jailbreak]({% post_url 2015-12-14-kindle-jailbreak %}) on our Kindle and installed a bunch of wonderful extensions. Now it's time to go deeper into the innards of the liberated e-reader and extend its capabilities even further.

1. Connecting to the Kindle via SSH from Raspberry Pi

	On Kindle, fire up KUAL and select *USBNetwork* -> *\* Toggle USBNetwork \**.
	Plug your Kindle into Raspberry Pi via USB (I'm assuming you have a 
	working Raspberry Pi set up already, with keyboard/mouse, a monitor 
	and a wifi dongle). Since mass storage mode is incompatable with SSH, 
	eject Kindle.
	
	Now on Raspberry Pi:
	
		# ifconfig usb0 192.168.15.201

	Test if you can connect via SSH yet:

		# ssh root@192.168.15.201

	It will ask for a password, just hit Enter. You are in! Well, at least you should be. Refer to the enclosed README_FIRST in USBNetwork folder  if you are in trouble.

2. Make your future logins more swoosh with shared keys

	First, let's get rid of 192.168.15.201 by adding this line to your /etc/hosts:
		
		192.168.15.244 kindle

	Now on to the keys themselves:
		
		cd ~/.ssh
		ssh-keygen -C "Our Kindle key" -f id_kindle

	Enter your favorite passphrase. You should have id_kindle and id_kindle.pub. Let's copy your public key to the Kindle:

		scp id_kindle.pub root@kindle:/mnt/us/usbnet/etc/authorized_keys

	That's it! To make SSHing even more automatic, try things with ssh agent and keychain.

3. Install Extend

	Extend ([home][extend-home]) - additional command line tools, most importantly - ssh client, which is crucial for our end goal. 
	
	* [Download][extend-link] Extend

		Place extend and extensions folder in the root directory of your Kindle. You can do it either via usual USB connection or through SSH.
	
	* Next, connect to your Kindle via SSH and execute following commands:
		
			# ./mnt/us/install.sh
			# ln -s /mnt/us/circles/mountd /etc/rc5.d/S101mountd

		That should be it. We are now ready for the final step on this rather dragged out journey to Kindleberry Pi. 

[extend-home]: http://www.mobileread.com/forums/showthread.php?t=161704
[extend-link]: http://ge.tt/9Qoa9YD/v/2
