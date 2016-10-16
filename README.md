Universal installer for Odroid XU3/XU4
======================================

About
-----

Universal installer which can install **android**, **linux** or both (**dualboot**) from SD Card and/or USB drive.

**Features**

- based on Linux initramfs
- **interactive** installer
- user can set desired partition sizes and installation destination
- can install to **SD Card** and to **EMMC**
- uses standard Android **upgrade.zip** and Linux **image files** as sources
- Android installation source (update.zip) can be placed on **SD Card** or **USB drive**
- Linux installation source **must** be placed on **USB drive**
- installation sources must be placed on the **first** USB drive partition (ext4 or vfat formated)
- supports **dual boot installation** (Android & Linux)
- tested with all Android and Linux versions for XU3/XU4

**Usage**

- build the installer sdcard/image running `sudo ./prepare_selfinst <destination_card>|<destination_image_name> [full]`
- or you can use **prepared images**, unzip install_boot[_2GB].img.zip and run `sudo dd if=install_boot[_2GB].img of=/dev/sdX bs=1MB oflag=direct`
- 200MB sdcard/image will be prepared, if the 2nd parameter is **full** 2 GB image or full size sdcard will be prepared
- if the image file is created, you can write the image to SDCard using dd command.
- you can **expand** the FAT partition on SDCard to fit the SDCard size if you want, be careful **not to change** the partition **start sector**
- copy your installation sources (Android update image **update.zip**, Linux **.img** file) to the first partition of your USB drive
- **rename** the Linux installation image to **linux.img** !
- if you want to install **only Android**, you can copy **update.zip** to the SDCard, you don't need to use USB drive
- set Odroid **boot switch** to boot from SDCard
- connect you USB drive to Odroid (if used), insert SDCard and power on
- follow the instructions to select desired partition sizes and installation destination (**SDCard** or **EMMC**)
