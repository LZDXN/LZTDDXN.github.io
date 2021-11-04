以ubuntu为例：

1. 备份源文件source.list
```
sudo cp /etc/apt/sources.list /etc/apt/sources.list.bak
```
2. 修改源文件（直接用text editor）
```
sudo gedit /etc/apt/sources.list
```
打开之后把所有的源都替换成国内的
比如说中科大：http://mirrors.ustc.edu.cn/help/ubuntu.html
中科大的repository file generator: https://mirrors.ustc.edu.cn/repogen/
3. 关闭之后就可以
```
sudo apt update -y && sudo apt upgrade -y
```
and probably
```
sudo apt-get update -y && sudo apt-get dist-upgrade -y
```
(Note: 实战证明，21.04中科大源不支持 ```sudo apt-get update```)
同时也可以直接打开设置找到