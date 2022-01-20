dwm - dynamic window manager
============================
dwm is an extremely fast, small, and dynamic window manager for X developed by the [suckless team](https://dwm.suckless.org/)

This is my fork of their work with these patches:
[actual fullscreen](https://dwm.suckless.org/patches/actualfullscreen/)
[color bar](https://dwm.suckless.org/patches/colorbar/)
[cool autostart](https://dwm.suckless.org/patches/cool_autostart/)
[hide vacant tags](https://dwm.suckless.org/patches/hide_vacant_tags/)
[inplace rotate](https://dwm.suckless.org/patches/inplacerotate/)
[scratchpad](https://dwm.suckless.org/patches/scratchpad/)
[statuscmd](https://dwm.suckless.org/patches/statuscmd/)
[sticky](https://dwm.suckless.org/patches/sticky/)
[swallow](https://dwm.suckless.org/patches/swallow/)
[vanity gaps](https://dwm.suckless.org/patches/vanitygaps/)
[warp](https://dwm.suckless.org/patches/warp/)

Requirements
------------
In order to build dwm you need the Xlib header files.


Installation
------------
Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if
necessary as root):

    make clean install


Running dwm
-----------
Add the following line to your .xinitrc to start dwm using startx:

    exec dwm

In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:

    DISPLAY=foo.bar:1 exec dwm

(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something
like this in your .xinitrc:

    while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
    do
    	sleep 1
    done &
    exec dwm


Configuration
-------------
The configuration of dwm is done by creating a custom config.h
and (re)compiling the source code.
