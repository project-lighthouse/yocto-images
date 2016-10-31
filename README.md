# Project Lighthouse Yocto Images

Repository contains various Yocto images for the Project Lighthouse.

__Latest release__: [v0.0.5](https://github.com/project-lighthouse/yocto-images/releases/v0.0.5)

# Instructions

To save space, network bandwidth and accommodate all possible SD Card sizes main partition is only 1GB by default. During the first boot partition will be expanded automatically.

Example:

1. Download and unpack `image-va.b.c.zip`;
2. Write image to your SD Card as described [here](https://www.raspberrypi.org/documentation/installation/installing-images/);
3. [OPTIONAL] If you'd like to configure bootstrap sequence, then mount SD Card boot partition on your laptop and edit `scripts/bootstrap.sh` script;
4. Insert SD card to the RPi2, make sure that it's connected to the LAN with Internet access and turn it on;
5. First boot can take up to 4 minutes, depending on your SD Card size, performance and quality of internet connection;
6. Enjoy!

Once your RPi is ready you can also do the following:

* Establish SSH session:
    * `$ ssh root@lighthouse.local`
* Enable Samba (once your established SSH session):
    * `$ smbpasswd -a root`
    * Choose password you want to use for your Samba share
    * Access/mount shared drive using `root` user and password you set at the previous step