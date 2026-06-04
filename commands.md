# Commands Used

```bash

lsblk                            = Lists all attached storage devices and partitions.

df -h                            = Displays disk usage and mounted storage in human-readable format.

mkfs.ext4 /dev/nvme3n1           =   Creates an EXT4 filesystem on the new EBS volume.

mkdir /testdata                  =   Creates a directory to mount the EBS volume.

mount /dev/nvme3n1 /testdata     =   Attaches the EBS volume to the Linux filesystem.

echo "Backup Test by Viren" > /testdata/test.txt       =   Creates a sample file for backup testing.

echo "Customer Data" > /testdata/customer.txt          =    Creates a sample customer data file.

echo "AWS Disaster Recovery Project" > /testdata/project.txt       =    Creates a sample project data file.

ls -l /testdata                  =    Lists all files stored on the EBS volume.

rm -f /testdata/*                =    Deletes files to simulate a disaster or accidental data loss.

mkdir /restoretest               =    Creates a directory for mounting the restored volume.

mount /dev/nvme4n1 /restoretest  =    Mounts the volume restored from the snapshot.

ls -l /restoretest               =    Confirms that files were successfully recovered from the backup.

```
