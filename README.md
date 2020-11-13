# x220-coreboot

My last coreboot built for the thinkpad x220 with 2 different configurations:

1) m4rc0linux220coreboot.rom - featuring vga bootsplash and support to intel wifi cards and bluetooth
2) x220m4rc0.rom - featuring lbgfxinit set to 1024x768 (bootsplash1 included), no support to intel wifi and bluetooth - this is my last, and more free, built.

In both cases include seabios with all the secondary payloads, boot menu wait set to 1 sec, and me_cleaner applied

Ram frequency has been fixed. it works well with ddr3 1600 setting correctly the speed on 800mhz x 2 channels. In my previous version and the oem bios this is limited to 667 mhz.

Both roms are meant to be flashed externally and it is just a starting point for you own builds. Have a look to the .config file, which you can use and modify.

The Seabios wait time has been reduced to 1 sec only, applying  ./build/cbfstool build/coreboot.rom add-int -i 1000 -n etc/boot-menu-wait as described in the official guide: https://www.coreboot.org/SeaBIOS

Bootsplash has been originally downloaded from this post https://www.reddit.com/r/thinkpad/comments/ggomje/another_finished_project_t420_coreboot_with/  
Bottsplash1 has been made by myself modifying the classical x220 exploded wallpaper (colours will work good with libgfxnint)

if you already have coreboot installed, you can fash it internally with sudo flashrom -p internal:laptop=force_I_want_a_brick -c MX25L6405 -w "name".rom -V

It is intended to be used on the "normal" thinkpad x220. It won't work on different models like x220i or x220t 

There is no warranty or support guaranteed so please keep this in mind if you intend to use this software. I am not responsible for broken devices.

To see how this (or my others built images) works, just have a look into my youtube https://www.youtube.com/user/marcolinoxz
