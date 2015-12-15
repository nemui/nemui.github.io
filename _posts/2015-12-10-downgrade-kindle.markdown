---
layout: post
title:  "Downgrading Kindle Paperwhite (1st generation)"
date:   2015-12-10 10:36:18 +0900
categories: kindleberrypi kindle downgrade
---
First step on the way to your very own [Kindleberry Pi][kindleberry-pi] is
downgrading your Kindle:

1. Turn on the airplane mode

	While jailbreak itself should survive firmware updates, custom hacks it enables might not. Proceed at your own risk. 

2. Download firmware

	At the time of writing, the most recent jailbreak works with firmware version 5.4.4.2. With a bit of URL trickery, we can [download it][firmware] from Amazon.

3. Copy the firmware to the Kindle root directory.

	Do not disconnect or eject your Kindle just yet. Instead, restart it by long pressing the power button on the bottom edge. Update progress dialogue should appear.

4. Confirm that downgrade went well

	From *Home* screen, tap *Menu*, then *Settings*.  
From *Settings* screen, tap *Menu* again, then *Device Info*.  
**Firmware Version:Kindle 5.4.4.2** means we are golden and ready to
[jailbreak]({% post_url 2015-12-14-kindle-jailbreak%}).

5. Make sure your Kindle is still yours

	It seems like downgrading can unregister your device. If that's
the case, simply register it again.	

[kindleberry-pi]: http://maxogden.com/kindleberry-wireless.html
[firmware]: https://s3.amazonaws.com/G7G_FirmwareUpdates_WebDownloads/update_kindle_5.4.4.2.bin 
