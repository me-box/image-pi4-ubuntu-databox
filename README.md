# image-pi4-ubuntu-databox
Ubuntu Server 19.10 image, with Docker and Databox installed, for Raspberry Pi 4 Model B

This image was built based on the [official release](https://ubuntu.com/download/raspberry-pi) of Ubuntu Server 19.10, with Docker 19.03.2 and Databox 0.5.2 installed.

## Bug fixes
1. The [USB bug](https://bugs.launchpad.net/ubuntu/+source/linux-raspi2/+bug/1848790) in the official release was fixed by updating the kernel following the steps in #25 in the bug report.
2. The keyboard layout was fixed to UK keyboard.

## Download
[Link](https://drive.google.com/file/d/11Z9EmReAr5mEn8QwlKU_coLJW_O4RTra/view?usp=sharing)

## How to use this image?
You need an SD card and to follow the [official instructions](https://ubuntu.com/download/iot/installation-media) to use this image.

## Login name and password
**login: ubuntu**

**default password: databoxubuntu**

**NOTE: Once you have logged in, change your password by `sudo passwd ubuntu`**

## How to run Databox using this image?
The `Makefile` in the directory `~/databox` can help you start (`make start-box`), stop (`make stop-box`), or restart (`make restart-box`) Databox. Be carefull that `make clean-all` will clean **ALL** the Docker containers, images, and volumes.

Before start Databox, take a record of the IP address of your Pi 4 (it should be shown on the terminal after you login, or you can use command `ip addr` to find it). Once you have started Databox on your Pi 4, you can use a browser on another computer to access the Databox through the ip address.
