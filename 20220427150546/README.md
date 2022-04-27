# How to Mount a USB Drive via Ubuntu VM

The pre-requisite for this work, is that you've already set up the
Virtual Machine to expose the USB device. This is pretty standard and
there are a ton or articles on the web on how to do this.

My issue was not mounting the drive, but mounting it in a way where I
had read/write access to it. Using the standard `mount` command would
work, but root then owned the directory and, as a user, I could not do
anything other than view its contents.

Eventually I found that you had to specify the file system used, as well
as the current user ids. The script below does this in a nice, Unix-ey,
fashion.

```bash
#!/bin/bash

: "${my_uid:=`id -u`}"
: "${my_gid=`id -g`}"

sudo mount -t vfat /dev/sdb1 /media/usb -o "uid=$my_uid,gid=$my_gid"
```

    #linux #virutalmachine #vm #usb
