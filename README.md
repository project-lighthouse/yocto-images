# Project Lighthouse Yocto Images

Repository contains various Yocto images for the Project Lighthouse.

__Latest release__: [v0.0.3](https://github.com/project-lighthouse/yocto-images/releases/v0.0.3)

# Instructions

To save space, network bandwidth and accommodate all possible SD Card sizes main partition is only 1GB by default. So you definitely want to change the size of the root partition depending on your SD Card size.

Example:

1. Download and unpack `image-va.b.c.zip`;
2. Write image to your SD Card as described [here](https://www.raspberrypi.org/documentation/installation/installing-images/);
3. Resize your root partition:
  1. On Linux Host: just use GParted to resize ext4 partition;
  2. On RPi: follow [this guide] (https://www.youtube.com/watch?v=R4VovMDnsIE) (except that you don't need swap partition). That basically boils down to the following steps:
    1. `$ fdisk -uc /dev/mmcblk0 d 2 n p 2 139264 xxxxx`
    2. `$ reboot`
    3. `$ resize2fs -p /dev/mmcblk0p2`
    4. `$ reboot`
4. Enjoy!
