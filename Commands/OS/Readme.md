## Verify OS 

cat /etc/os-release

## In the EC2 CLI, verify the Apache httpd service is running:

systemctl status httpd.service

## Verify the web page is reachable locally:

curl -s localhost:80
