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
