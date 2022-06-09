## Install the stress test application:

sudo amazon-linux-extras install epel -y
sudo yum install -y stress

## Run the stress test on the EC2 instance:

stress --cpu 2 --timeout 300

It could take up to 10 minutes to increase the CPU utilization.

