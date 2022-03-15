# pi-see
Using the pi camera on a Raspberry Pi 4 B

## Create sd card
Download bullseye
Use Raspberry Pi Imager. Select Custom.
Use ``2021-10-30 raspberry pi os 32 bit
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
