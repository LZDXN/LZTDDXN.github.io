Table of contents
---
- [[#Prerequisites]]
- [[#Create a Jupyter Notebook folder optional if you want you can run in root]]
- [[#Generate the password]]
- [[#Config the Jupyter Notebook]]
- [[#Finish]]
- [[#Reference]]



# Prerequisites
Install Conda [[Build Machine Learning environment using Ubuntu system]]
Normally install notebook by `conda install jupyter notebook`
Now we can run Jupyter Notebook by typing `jupyter notebook`, we need to build a online jupyter note use some config

# Create a Jupyter Notebook folder (optional, if you want you can run in /root)
Command line go python:
```bash
python3
```

# Generate the password
```py
from IPython.lib import passwd 
passwd()
```
Follow the instruction and input the password you want, it will generate you a `sha1:` text, record this which will be used later.

# Config the Jupyter Notebook
`quit()` Python, then
```bash
jupyter notebook --generate-config
```
It will generate a config file
```bash
nano /root/.jupyter/jupyter_notebook_config.py
```
Add config at the beginning of this file:
```py
c.NotebookApp.allow_remote_access = True
c.NotebookApp.ip = "*"
c.NotebookApp.open_browser = False
c.NotebookApp.password = "sha1:xxxxxxxx"
c.NotebookApp.port = 6543
c.NotebookApp.notebook_dir = "/home/ubuntu/conda/jupyter_home"
```
- `.ip`: IP address that permit user enter the jupyter notebook, `*` means any IP is available.
- `.open_browser`: Ppen browser while start it
- `.password`: Password you entered and got in that python code
- `.port`: Port to enter
- `.notebook_dir`: Notebook folder path

`Ctrl+X` and save it, then `jupyter notebook` to run it.

# Finish
You can now access the notebook by `ip:port`, then enter the password you set. 
Done! 

# Reference:
[搭建jupyter-notebook-远程服务器](https://blog.csdn.net/gernie/article/details/105547370?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522162823864516780269831704%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=162823864516780269831704&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-1-105547370.first_rank_v2_pc_rank_v29&utm_term=jupyter+%E6%9C%8D%E5%8A%A1%E5%99%A8&spm=1018.2226.3001.4187)