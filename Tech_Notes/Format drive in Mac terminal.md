The website searching is useless, those forum will not answer questions correctly
So I learned by know the tool in terminal:
```
diskutil
```
once type *diskutil* in mac there will show up a bunch of things telling you how to use it

**list drive**
```
diskutil list
```
This command will help you know drives that connect to mac and tell you whether this disk is internal or external

**erase drive**
```
diskutil eraseDisk *FormatName* *NewNameOfTheVolume* *positionOfVolume*
```
for example (one successful case):
```
diskutil eraseDisk ExFAT what disk2
```
other's example:
```
diskutil eraseDisk JHFS+ UntitledUFS disk3
```