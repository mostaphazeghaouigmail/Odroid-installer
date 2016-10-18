Universal installer for Odroid XU3/XU4
======================================

About
-----

Universal installer which can install **android**, **linux**, **OpenELEC** or combinations (**multiboot**) from SD Card and/or USB drive.

**Features**

- based on Linux initramfs
- **interactive** installer
- user can set desired partition sizes and installation destination
- can install to **SD Card** and to **EMMC**
- uses standard Android **upgrade.zip**, Linux **image files** and OpenElec **upgrade tar** files as sources
- Android installation source (update.zip) can be placed on **SD Card** or **USB drive**
- Linux installation source **must** be placed on **USB drive**
- OpenELEC installation source **must** be placed on **USB drive**
- installation sources must be placed on the **first** USB drive partition (ext4 or vfat formated)
- supports **multi boot installation** (Android, Linux, OpenELEC)
- tested with latest Android, Linux and OpenELEC versions for XU3/XU4

**Usage**

- build the installer sdcard/image running `sudo ./prepare_selfinst <destination_card>|<destination_image_name> [full]`
- **or** use **prepared installer images**, unzip universal_install[_2GB].img.zip and run `sudo dd if=universal_install[_2GB].img of=/dev/sdX bs=1MB oflag=direct`
- if preparing the image, 200MB sdcard/image will be prepared, if the 2nd parameter is **full** 2 GB image wil be prepared
- if preparing the sdcard, maximum capacity sdcard will be prepared
- if the image file is created, you can write the image to SDCard using dd command.
- copy your installation sources (Android update image **update.zip**, Linux **.img**, OpenELEC **.tar** file) to the first partition of your USB drive
- **rename** the Linux installation image to **linux.img** !
- **rename** the OpenELEC installation tar to **oelec.tar** !
- if you want to install **only Android**, you can copy **update.zip** to the SDCard, you don't need to use USB drive
- set Odroid **boot switch** to boot from SDCard
- connect you USB drive to Odroid (if used), insert SDCard and power on
- follow the instructions to select desired partition sizes and installation destination (**SDCard** or **EMMC**)

**HINTS**
- select desired Android resolution in **boot.ini.android**, Hardkernel utility does not work
- after upgrading **Linux kernel**, first following reboot will be directly to Linux.
