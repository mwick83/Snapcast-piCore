You only need resize_sd.sh and install_snapclient.sh

Download both install scripts to a fresh piCore installation in the user's home:
```
$ cd ~
$ wget https://github.com/mwick83/Snapcast-piCore/raw/master/install_snapclient.sh
$ wget https://github.com/mwick83/Snapcast-piCore/raw/master/resize_sd.sh
```
Make the script executable:
```
$ chmod +x *.sh
```
Run the SD resize helper, so it has enough space. You need to do this only in case you didn't already as per the piCore installation instructions.
``` 
$ ./resize_sd.sh
``` 
after reboot run:
``` 
$ sudo resize2fs /dev/mmcblk0p2
```
Now install snapclient:
``` 
$ ./install_snapclient.sh
```

TBD: Document how to change the hostname.
TBD: Document how to enable hifiberry-amp, etc.
TBD: Modify install script to store alsa state (filetool.sh)

After reboot snapclient should autostart :)
To switch betwean HDMI and analog output use

HDMI:
```
$ amixer cset numid=3 2
```
Analog:
```
$ amixer cset numid=3 1
```
or just connect to the Webinterface on http://SnapCast-Client-IP
