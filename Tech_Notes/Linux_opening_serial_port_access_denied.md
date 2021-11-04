Problem
---
```
avrdude: ser_open(): can't open device "/dev/ttyusb0": Permission denied
```
or
```
Error opening serial port '/dev/ttyusb0
```
This happened when I use Arduino IDE in ubuntu 21.04 use Raspiberry Pi 4B model, and it tell me to visit https://support.arduino.cc/hc/en-us/articles/360016495679-Error-opening-serial-port-Linux-
Of course this problem was solved

Solution
---
Open terminal and type:
```
ls -l /dev/ttyusb0
```
Then it will show up:
```
crw-rw---- 1 root dialout 188, 0 5 apr 23.01 ttyACM0
```
In official site it says `/dev/ttyACM\*` well actually it depends on port we select (make sure it is the right port to Arduino)
What we are interested in is the group name, which is probably called `dialout`.
Then we give the permission by put user in group, typing:
```
sudo usermod -a -G <group> <username>
```
For example:
```
sudo usermod -a -G dialout lztd
```
Successful!
Then, use `groups` to verify if this permission take effect, but before that, reboot it (log out and sign in the account)
done :)