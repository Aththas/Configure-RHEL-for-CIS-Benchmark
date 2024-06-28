# 2. Disk Partitioning

## 2.1 Ensure /home Located On Separate Partition

#### 2.1.1 List Current Partitions (This displays the disk usage in a human-readable format)
  $ df -h

Check for '/home' in the output. If '/home' is not on a separate partition, We will use LVM to move '/home' in seperate partition.

#### What is LVM?
Logical Volume Manager (LVM) is a device-mapper framework that provides logical volume management for the Linux kernel. It allows for flexible disk management, enabling you to resize disk partitions, create snapshots, and move data between physical disks without downtime. LVM abstracts the underlying physical storage and provides a higher level of flexibility and control over disk space.

#### 2.1.2 Install LVM
  $ sudo yum install -y lvm2

#### 2.1.3 Load the Device-Mapper Kernel Module
  $ sudo modprobe dm_mod

#### 2.1.4 

