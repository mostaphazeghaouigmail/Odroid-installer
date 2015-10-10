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
- Linux installation source must be placed on **USB drive**
- installation sources must be placed on the first USB drive partition (ext4 or vfat formated)
- supports **dual boot installation** (Android & Linux)
- tested with all Android and Linux versions for XU3/XU4

**Usage**

- download prepared **universal installer** SDCard image (use **md5** to check the integrity of the downloaded files)
- unpack xz archive
- **`universal_install_small.img`** is 200MB image, **`universal_install.img`** is 2 GB SDCard image
- write the image to SDCard using dd command under Linux or image writing software under Windows.
- you can **expand** the FAT partition on SDCard to fit the SDCard size if you want, be careful **not to change** the partition **start sector**
- copy your installation sources (Android **update image** **update.zip**, Linux **.img** file) to the first partition of your USB drive
- rename the Linux installation image to **linux.img** !
- if you want to install **only Android**, you can copy **update.zip** to the SDCard, you don't need to use USB drive
- set Odroid **boot switch** to boot from SDCard
- connect you USB drive to Odroid, insert SDCard and power on
- follow the instructions to select desired partition sizes and installation destination (**SDCard** or **EMMC**)[/list]
