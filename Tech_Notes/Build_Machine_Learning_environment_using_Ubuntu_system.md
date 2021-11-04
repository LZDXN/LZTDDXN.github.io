# Requirements
(Using Ubuntu 20.04)
- Python 3
- [[#Installing]]
	- [[#Anaconda www anaconda com|Anaconda]]
	- [[#Jupyter Notebook https jupyter org|Jupyter Notebook]]
	- [[#Pandas https pandas pydata org|Pandas]]
	- [[#Numpy https numpy org|Numpy]]
	- [[#Pytables https www pytables org|Pytables]]
	- [[#SciPy https www scipy org|Scipy]]
	- [[#Matplotlib https matplotlib org|Matplotlib]]
	- [[#Mglearn https pypi org project mglearn|Mglearn]]
- [[#The Summary]]

Simple update:
```shell
sudo apt update -y && sudo apt upgrade -y
```


# Installing
## Anaconda (www.anaconda.com)
1. Install prerequisites 
	```shell
	apt-get install libgl1-mesa-glx libegl1-mesa libxrandr2 libxrandr2 libxss1 libxcursor1 libxcomposite1 libasound2 libxi6 libxtst6
	```
2. Download installer
	- via https://www.anaconda.com/products/individual#Downloads
		- (Using command line:) `wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh`
	- (require root permission) run this sh file  `bash ~/Downloads/Anaconda3-2020.02-Linux-x86_64.sh` or just `sh `then drop the file in terminal
	- Follow the instruction and finish install
3. When finish, use `conda init` to check if anaconda is installed successfully
4. If `conda` command does not exist, check the path of installation, then 
	Config the `~/.bashrc` file:
	```bash
	nano ~/.bashrc
	```
	Add this after the last line:
	```bash
	export PATH=$PATH:/path-to-installation
	#For example, my default path:
	export PATH=$PATH:/root/anaconda3/bin
	```
	Save it, then execute:
	```bash
	source ~/.bashrc
	```
	Then back to the third step, done.

Some useful commends ([Official Cheat Sheet](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf)):
```bash
# Commend of update
conda update PACKAGE
# Commend of install
conda install PACKAGE
# Create a new environment
conda create --name NAME python=VERSION
# List environments
conda env list
# Activate the new environment (Linux & Mac)
source activate NAME
```


## Jupyter Notebook (https://jupyter.org/)
**Using Conda**
```bash
conda install jupyter
```
When run it
```bash
jupyter notebook
```
Not recommend running this using root permission, ~~*I ran it anyway*~~, if so,
```bash
jupyter notebook --allow-root
```


## Pandas (https://pandas.pydata.org/)
**Using Conda**
```bash
conda install pandas
```


## Numpy (https://numpy.org/)
**Using Conda** (Should be installed in previous packages)
```bash
conda install numpy
```


## Pytables (https://www.pytables.org/)
**Using Conda** (Should be installed in previous packages)
```bash
conda install pytables
```


## SciPy (https://www.scipy.org/)
**Using Conda** (Should be installed in previous packages)
```bash
conda install scipy
```


## Matplotlib (https://matplotlib.org/)
**Using Conda** (Should be installed in previous packages)
```bash
conda install matplotlib
```


## Mglearn (https://pypi.org/project/mglearn/)
**Using pip**
```bash
pip3 install mglearn
```


# The Summary
Summary: I love $\color{green}\text{conda}$