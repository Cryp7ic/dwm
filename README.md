Dynamic Window Manager (dwm)
============================

Installation
------------
```shell
$ mkdir ~/.sources
$ cd ~/.sources
$ git clone https://github.com/Cryp7ic/dwm.git
$ cd dwm
# make clean install
```


Running dwm
-----------
Add the following line to your .xinitrc to start dwm using startx:

    dwm

If it does not work, do this:

```shell
$ which dwm
/usr/local/bin/dwm
```

Then add this to .xinitrc:

```shell
/usr/local/bin/dwm
```

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
