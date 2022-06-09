## Creating and Restoring a Linux EC2 Snapshot

## Create a Snapshot for backup 

## Create a New Volume from snapshot

Attach it to the Ec2 instance

In the EC2 CLI, verify the contents of /mnt:

ls /mnt
Remove the important-stuff.txt file:

rm /mnt/important-stuff.txt
Enter y to confirm removal.

Verify the file has been removed:

ls /mnt

In the EC2 CLI, list the block devices:

lsblk

Mount the partition:

mount /dev/xvdg1 /new_vol

Confirm the new mount was successful:

df

List the contents of /new_vol:

ls /new_vol

Restore the file:

cp /new_vol/important-stuff.txt /mnt

Confirm the file has successfully been restored:

ls /mnt
