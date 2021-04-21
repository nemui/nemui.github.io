+++
title = "Downgrading Kindle Paperwhite (2012)"

[taxonomies]
tags = ["kindleberrypi", "kindle", "downgrade"]
+++
First step on the way to your very own [Kindleberry Pi][kindleberry-pi] is
downgrading your Kindle:

1. Turn on the airplane mode

	While jailbreak itself should survive firmware updates, custom hacks it enables might not. Proceed at your own risk. 

2. Download firmware

	At the time of writing, the most recent jailbreak works with firmware version 5.4.4.2. With a bit of URL trickery, we can [download it][firmware] from Amazon.

3. Copy the firmware to the Kindle root directory.

	Do not disconnect or eject your Kindle just yet. Instead, restart it by long pressing the power button on the bottom edge. Update progress dialogue should appear.

4. Confirm that downgrade went well

	From _Home_ screen, tap _Menu_, then _Settings_.  
From _Settings_ screen, tap _Menu_ again, then _Device Info_.  
**Firmware Version:Kindle 5.4.4.2** means we are golden and ready to [jailbreak](@/blog/2015/2015-12-14-kindle-jailbreak.md).

5. Make sure your Kindle is still yours

	It seems like downgrading can unregister your device. If that's
the case, simply register it again.	

[kindleberry-pi]: http://maxogden.com/kindleberry-wireless.html
[firmware]: https://s3.amazonaws.com/G7G_FirmwareUpdates_WebDownloads/update_kindle_5.4.4.2.bin 
