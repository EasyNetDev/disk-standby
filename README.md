# disk-standby
Disk tool for setting and loading standby timeouts HDD

## What is it?
This is a very simple tool that is using hdparm as backend to set, save and load standby timeoutconfiguration for disk.

## Why?
I developed this tool to use it under Proxmox enviroment, which is a Debian Linux distribution and it doesn't have a tool in GUI to set standby timeouts for disks, like TrueNAS Scale.
For this reason I created this small tool which sets the standby timeout for a disk or multiple disks and it saves their config in /var/lib/hdparm/disk-standby in a simple form.
Then, using a systemd service called disk-standby.service can load the configuration at the boot time.
Is easy for me to use a command line tool and set/unset this parameter for a batch of disk instead all the time to modify /etc/hdparm.conf

