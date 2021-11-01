What I am doing now is burning the ubuntu file into my sd card, I don't know if it will work but I will do it anyway

I use the terminal
```
diskutil list
```
list all drives connected to computer, find the one looks like volume of sd card.
Then unmount it(for example disk2):
```
disktuil unmountDisk /dev/disk2
```
When it tells you unmount successfully, erase this drive by replacing the ISO image, make sure select the right identifier to avoid the unintended data loss
```
sudo dd if=/path/to/iso-file of=/dev/disk2 bs=1m
```
==**The process will start immediately and there is no progress bar, be patient!**==
While it finished, it will ask you this disk is not readable (ubuntu), so eject it

![[Pasted image 20210607095856.png]]

In fact, this way burning ubuntu 20.04 iso file into sd card is not readable in raspberry pi 4b model booting

~~*fucking useless*~~

==**Update:**== The official Ubuntu 20.04 LTS does not support raspberry pi... but 21.04
OK fine
Looks like it is functional