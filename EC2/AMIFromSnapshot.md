## Create Custom AMI and Launch new instance 

## Install httpd:
yum install -y httpd
systemctl enable httpd.service
systemctl start httpd.service
curl -s localhost | head
echo "Hello World" > /var/www/html/index.html
curl -s localhost | head


## Create a New AMI

Stop the Instance 
Create Snapshot 
Create AMI from Snapshot 
Launch new instance from Custom AMI 
