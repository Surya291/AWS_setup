## Step 01 : Create a venv with python> 3.7

To change Python 3.6.8 as the default in Ubuntu 18.04 to Python 3.7.
Install Python 3.7
Steps to install Python3.7 and configure it as the default interpreter.
Install the python3.7 package using apt-get
```
sudo apt-get install python3.7
```
Add Python3.6 & Python 3.7 to update-alternatives
```
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.6 1
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.7 2
```
Update Python 3 to point to Python 3.7
```
sudo update-alternatives --config python3 Enter 2 for Python 3.7
```
Test the version of python

python3 --version
Python 3.7.1 



## Step 02 : Allow port 8080 (default for label studio) in AWS security groups 
```
Follow these steps to do this:

Open "Network & Security" -- Security Group settings are on the left-hand navigation
Find the security group connected to your instance
Choose “inbound rules”
Type the port number (in your case 8787) in “port range” then click “Add Rule”
Use the drop-down and add HTTP (port 80)
And it is done.
```

## Step 03 : Specify an external domain for label studio while starting 
```
label-studio start --host http://55.195.155.195:8080/
```
NOTE : the domain is Public IPv4 address of the VM


## MISC : Fin and closing labelstudio  ports 
```
killall -i label-studio

Alternative soln
sudo kill -9 $(sudo lsof -t -i:8080)
```
