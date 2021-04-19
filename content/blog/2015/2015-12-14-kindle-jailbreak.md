+++
title = "Kindle Jailbreak"

[taxonomies]
tags = ["kindleberrypi", "kindle", "jailbreak"]
+++
After [downgrading our Kindle](@/blog/2015/2015-12-10-downgrade-kindle.md),
we proceed to installing the jailbreak itself.
All information was pulled from [this forum thread][jailbreak-thread].

1. Download the [jailbreak][jailbreak-link]

	Inside the archive you will find kindle-5.4-jailbreak.zip - extract it
to the root directory of your Kindle. Eject and unplug.

2. Make your Kindle better by breaking it

	Go to *Home* screen, tap *Menu* and select *Settings*. Tap *Menu* again and select *Update Your Kindle*. For a few terrifying moments, nothing will
happen, then the words \*\*\*\* JAILBREAK \*\*\*\* should appear at the bottom
of the screen. It's done! Restart your Kindle for good measure.

3. Install cool hacks

	* USBNetwork ([home][jailbreak-thread]) - makes it possible to login
	into your Kindle over usb or wifi. Neat!

		Grab [the archive][usbnet-link], locate Update_usbnet_0.21.N_i
		nstall_touch_pw.bin and install it the same way as the jailbreak
		.

	* KUAL ([home][kual-home]) - kindle unified application launcher
	
		After [downloading][kual-link], locate KUAL-KDK-2.0.azw2 and
		place it in the /documents directory of your Kindle. That's it -
		now you have a shiny new "book" on your shelf.
		
	* KUAL helper ([home][helper-home]) - adds "Helper" menu with a bunch of
	useful functions to KUAL

		Download [extension][helper-link] and copy helper directory
		to /documents/extensions (create extensions folder if it
		doesn't exist yet). Every other extension is installed in a
		similar fashion.

	* GAWK ([home][gawk-home]) - makes KUAL's parsing faster

		Download [gawk][gawk-link] and install it just like the KUAL 
		helper from before. One additional step - open KUAL and press 
		"Install" button.
		
	* BackDoorLock ([home][lock-home]) - prevents silent updates

		Download [backdoorlock][lock-link] and install, you know the
		drill by now. Enable it via KUAL. Now the airplane mode can be
		safely turned off.

4. Explore the rest of the available [KUAL extensions][ext-link] and [Kindle Paperwhite hacks][hacks-link] 

[jailbreak-thread]: http://www.mobileread.com/forums/showthread.php?t=186645  
[jailbreak-link]: http://www.mobileread.com/forums/attachment.php?attachmentid=141182&d=1439936183
[kual-home]: http://www.mobileread.com/forums/showthread.php?t=203326
[kual-link]: http://www.mobileread.com/forums/attachment.php?attachmentid=142287&d=1443189086
[helper-home]: http://www.mobileread.com/forums/showthread.php?t=203326
[helper-link]: http://www.mobileread.com/forums/attachment.php?attachmentid=141192&d=1439936781
[gawk-home]: http://www.mobileread.com/forums/showpost.php?p=2636883&postcount=50
[gawk-link]: http://www.mobileread.com/forums/attachment.php?attachmentid=141191&d=1439936739
[lock-home]: http://www.mobileread.com/forums/showpost.php?p=2423767&postcount=25
[lock-link]: http://www.mobileread.com/forums/attachment.php?attachmentid=132675&d=1418976828
[usbnet-link]: http://www.mobileread.com/forums/attachment.php?attachmentid=141348&d=1440341950
[ext-link]: http://www.mobileread.com/forums/showthread.php?t=205064
[hacks-link]: http://wiki.mobileread.com/wiki/Kindle_Touch_Hacking
