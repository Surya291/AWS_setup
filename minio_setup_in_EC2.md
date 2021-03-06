# Setting Up Minio Server on AWS Ec2 Instance
​
## Launching AWS Server and accessing it via ssh
- Login on the aws services website using the credentials.
- Create an ec2 Instance using the default options (Use Amazon Linux)
- Go to the folder containing the key pair file. (The file would be downloaded when you launch the client).
- ssh to the server using `ssh -i "path to key-pair file" ec2-user@"ipv4 public dns"`
​
## Seting Up Minio Server
- After getting the ssh access to the vm terminal, run the following commands :
​
    - ```wget https://dl.minio.io/server/minio/release/linux-amd64/minio```
​
    - ```chmod +x minio```
    - ```sudo ./minio server /minio```
​
- The server will start on the localhost of VM.
​
## Start Httpd service and provide access to the port
​
- Start the httpd service on the vm (https://www.cyberciti.biz/faq/star-stop-restart-apache2-webserver/)
​
- On the instance dashboard of aws, edit the inbound rules and allow the port on which the minio server is running.
​
- The minio server can now be accessed on "ip.address": port_number

Try to allow a ports for http and tcp in AWS while going to security section for the respective instance.
