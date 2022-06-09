## Verify OS 

cat /etc/os-release

## In the EC2 CLI, verify the Apache httpd service is running:

systemctl status httpd.service

## Verify the web page is reachable locally:

curl -s localhost:80

## Install httpd:
yum install -y httpd

## Enable the httpd service so it starts at boot:

systemctl enable httpd.service

## Start the httpd service:

systemctl start httpd.service

## View the test page for the Apache HTTP server:

curl -s localhost | head


echo "Hello World " > /var/www/html/index.html
## View the test page again:

curl -s localhost | head

