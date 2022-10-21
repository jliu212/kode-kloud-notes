# Sotrage in Linux

## Disk partitions

`lsblk` to list the hardware
`ls -l /dev/ | grep "^b"` ls the look at the fiels in the /dev folder with file type b
major number is te device type, minor number is the partition
information is stored in a partition table

fdisk to print parition table

### Parition type

MBR:

- Primary parition - to boot OS, no more than 4, if you want more thatn 4 needs to use extented parition
- Extended parition - contains partition table that point to logical partition
- Logical Partition - contained within extentied partition

GTP scheme has unlimited partition

### Create partition

`gdisk /dev/` gpt based parition

## File system in linux

## DAS NAS and SAn

## LVM
