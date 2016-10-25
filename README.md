# Project Lighthouse Yocto Images

Repository contains various Yocto images for the Project Lighthouse.

__Latest release__: [v0.0.2](https://github.com/project-lighthouse/yocto-images/releases/v0.0.2)

# Instructions

To save space, network bandwidth and accommodate all possible SD Card sizes main partition is only 1GB by default. So you definitely want to change the size of the root partition depending on your SD Card size.

Example:

1. Download and unpack `image-va.b.c.zip`;
2. Write image to your SD Card as described [here](https://www.raspberrypi.org/documentation/installation/installing-images/);
3. Open your favorite disk manager (eg. GParted, fdisk + resize2fs etc.) and resize the second partition as you like;
4. Enjoy!
