# Setup instance
## Ensure the OS 
## increase the memory

### download the pem key 
```
Open an SSH client.
Locate your private key file. The key used to launch this instance is lk-ubuntu-server.pem
Run this command, if necessary, to ensure your key is not publicly viewable.
 chmod 400 lk-ubuntu-server.pem
Connect to your instance using its Public DNS:
 ec2-18-208-219-13.compute-1.amazonaws.com
Example:
 ssh -i "lk-ubuntu-server.pem" ubuntu@ec2-18-208-219-13.compute-1.amazonaws.com
 ```
### Update pip
sudo apt update
sudo apt install python3-pip

## Create a venv
source LK-env/bin/activate

## Copy paste nemo contents
## copy requirements.txt to LK-env >> pick from github(this repo)

## Update pip and setup tools in venv else gives "python setup.py egg_info" failed with error code 1"
```
$ pip3 install --upgrade setuptools
$ pip3 install --upgrade pip
```

## Install requirements.txt >> pick from github



