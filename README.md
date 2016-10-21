# Project Lighthouse Yocto Images

Repository contains various Yocto images for the Project Lighthouse.

__Latest release__: [v0.0.1](https://github.com/project-lighthouse/yocto-images/releases/download/v0.0.1/image-v0.0.1.zip)

# Instructions

To save space, network bandwidth and accommodate all possible SD Card sizes main partition is only 1GB by default. So you definitely want to change the size of the image before writing it to the SD Card.

For example if you'd add 1GB of free space for your image:

## Linux

1. Unpack `image-va.b.c.zip`
2. `$ dd if=/dev/zero bs=1024 count=1048576 >> image-va.b.c.img`
3. `$ parted image-va.b.c.img resizepart 2 2048`
4. Write resulting image to your SD Card as described [here](https://www.raspberrypi.org/documentation/installation/installing-images/)