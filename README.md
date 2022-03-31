# pi-see
Using the pi camera on a Raspberry Pi 4 B

## Create sd card
- Download bullseye
- Use Raspberry Pi Imager.
- Select use custom.
- Choose ``2021-10-30-raspios-bullseye-armhf-full.img``
- Write SD card

> Used image from https://downloads.raspberrypi.org/raspios_armhf/images/raspios_armhf-2021-11-08/
> TODO verify with other images.

## Setup OS
Skip setup
Run raspi-config
Interfaces tab
- select camera
- select ssh

> HDMI port may switch

## use camera

### ssh into the RPI

Run ``libcamera-vid -t 0 --inline --listen -o tcp://0.0.0.0:8888``

### On another machine on the LAN
- In VLC, select Media > Open Network Stream
- enter ``tcp/h264://raspberrypi.local:8888``

## Links and references

https://www.raspberrypi.com/documentation/accessories/camera.html

https://projects.raspberrypi.org/en/projects/getting-started-with-picamera/3

https://github.com/geerlingguy/pi-webcam

https://www.tomshardware.com/how-to/use-raspberry-pi-camera-with-bullseye
