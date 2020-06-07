# x220-coreboot
My coreboot built for the thinkpad x220, including vga bootsplash, boot menu wait set to 1 sec, and me_cleaner

the m4rc0linux220coreboot.rom is meant to be flashed externally and it is just a starting point for you own builds. Have a look to the .config file, which you can use and modify (if you wish to build your own is hightly recommended to change the vga options othewise no image will appear or eventually the the device won't boot at all.

The Seabios boot time has been reduced to 1 sec only, applying $ ./build/cbfstool build/coreboot.rom add-int -i 1000 -n etc/boot-menu-wait as described in the official guide: https://www.coreboot.org/SeaBIOS

the amazing bootsplash has been downloaed from a reddit post however I am unable t find the original post. Feel frree to change it. 

if you already have coreboot installed, you can fash it internally.

It is intended to be used on the "normal" thinkpad x220. It won't work on different models like x220i or x220t 

There is no warranty or support guaranteed so please keep this in mind if you intend to use this software. I am not responsible for broken devices.

To see how it works just have a look into my youtube https://www.youtube.com/user/marcolinoxz
