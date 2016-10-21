# Project Lighthouse Yocto Images

Repository contains various Yocto images for the Project Lighthouse.

__Latest release__: [v0.0.1](https://github.com/project-lighthouse/yocto-images/releases/download/v0.0.1/image-v0.0.1.zip)

# Instructions

To save space, network bandwidth and accommodate all possible SD Card sizes main partition is only 1GB by default. So you definitely want to change the size of the image before writing it to the SD Card.

For example if you'd like to add 1GB of free space for your image, you'd follow the steps below:

## Linux

1. Unpack `image-va.b.c.zip`
2. `$ dd if=/dev/zero bs=1024 count=1048576 >> image-va.b.c.img`
3. `$ parted image-va.b.c.img resizepart 2 2048`
4. Write expanded image to your SD Card as described [here](https://www.raspberrypi.org/documentation/installation/installing-images/linux.md)

## Mac OS

1. Unpack `image-va.b.c.zip`
2. Run linux docker container with mounted folder containing unpacked image: `$ docker run -it --name resizer -v /folder_with_unpacked_image_file/:/image azasypkin/img-resizer:0.1`
3. Inside container: `$ dd if=/dev/zero bs=1024 count=1048576 >> /image/image-va.b.c.img`
4. Inside container: `$ parted /image/image-va.b.c.img resizepart 2 2048`
5. Write expanded image to your SD Card as described [here](https://www.raspberrypi.org/documentation/installation/installing-images/mac.md)