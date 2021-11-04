To update python 3 version in Raspberry Pi, I searched method online, looks like there are various ways to do that I would choose one of them

To begin with, get root permission and go to the folder `/usr/src/`
```bash
sudo su
cd /usr/src/
```
Download tgz file from official website:
```bash
wget https://www.python.org/ftp/python/3.x.x/Python-3.x.x.tgz
```
Unzip it:
```bash
tar -xvzf Python-3.x.x.tgz
```
cd into the folder(tab for convenience):
```bash
cd Python-3.x.x
./configure --enable-optimizations
```
After the make file is ready(takes long time, be patient):
```bash
make
```
then:
```bash
sudo make install
```
Finally, clean up the downloading zip file and folder (optional)
(Back to /usr/src/ first)
```bash
rm -Rf Python-3.x.x
rm Python-3.x.x.tgz
```