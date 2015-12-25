---
layout: post
title:  "Kindleberry Pi: The End"
date:   2015-12-25 14:28:18 +0900
categories: kindleberrypi kindle raspberrypi
---
Well, this is rather embarrassing.

This project was finished almost two weeks ago, and as a result - immediately
forgotten. I guess getting there was far more exciting than playing with the 
resulting contraption.

After the [last step]({% post_url 2015-12-15-usbnetwork-extend %}), the only 
things 
left to do are to install Kterm, create basic "extension" to automate 
connection process and setup an access point on Raspberry Pi. With first two 
you can pretty much follow [Rod Vagg's tutorial][guide-link] to the letter
(including the custom build part). For private ssh key, I re-used the pair
created when setting up USBNetwork.

Concerning AP on Raspberry Pi, I found [this post][hostapd-link] to be extremely
helpful.

So, my final setup is:

* Raspberry Pi 2 Model B
* Kindle Paperwhite 1st generation
* Two Planex GW-USNANO2A Wi-Fi dongles
* Planex Micro4 Bluetooth dongle
* Microsoft Universal Mobile Keyboard
* Anker Powercore+ 10050

While vimming aroung is pretty neat, small terminal size combined with 
ghost characters and absence of color makes it rather hard to enjoy roguelikes 
([DCSS][dcss-link], I'm looking at you). Oh well! Maybe I will find ways to alleviate some of its shortcomings, or simply re-purpose the whole setup. 

For now, though, I'm content to let my Kindleberry Pi gather dust.

[guide-link]: https://gist.github.com/rvagg/5095506
[hostapd-link]: http://cberner.com/2013/02/03/using-hostapd-on-ubuntu-to-create-a-wifi-access-point/
[dcss-link]: https://crawl.develz.org
