# Getting started with our Raspberry Pi

Hello, in front of you is Raspberry Pi 3 or Raspberry Pi 5 loaded with a default Raspbian OS Lite (with no GUI/Desktop).  
In case you would want to flash this image onto your device, ask one of the mentors to provide you with the image.

## Network / How to connect

### Wi-Fi

Raspberry is set to connect automatically to provided wifi network.  
IP address is assigned by our DHCP server.  
To find an IP for your Raspberry check the label on the board.  
It's going to be 10.10.1.[raspi number]. I.e.:  
RasPi01 = 10.10.1.1  
RasPi02 = 10.10.1.2  
and so on...

RasPi5-03 = 10.10.1.53
...

### Ethernet

Current setup counts on you connected to your raspi only through WiFi, so if you need direct ethernet connection, you have to it up yourself. 

Note: Do not set up static IP address when connected to our network. Do it only when you need to connect the rpi directly into your machine using cable. 


## Access & Passwords

Available connections:

* SSH for CLI.
* SFTP/SCP for file transfer.

!! Passwords are the same for all the boards.  
!! Please change them to your own as a first step to prevent access of the other teams to your device.

| Account | Password  |
| ------- | --------- |
| root    | raspiroot |
| pi      | raspipi   |

## Connectivity

Schematics: https://www.jameco.com/Jameco/workshop/circuitnotes/raspberry-pi-circuit-note.html  
GPIO pinout details: https://pinout.xyz

## Sense HAT

Python library is already present in the Raspbian OS.  
Sense HAT provides following for the Raspberry:  

* Temperature
* Humidity
* Barometric pressure
* Gyroscope
* Acceletometer
* Magnetometer
* Joystick
* 8x8 RGB LED matrix

API reference: https://pythonhosted.org/sense-hat/api/  
Tutorial: https://www.raspberrypi.com/documentation/accessories/sense-hat.html
  
## Pi AI Camera

**Specs:**  
https://www.raspberrypi.com/products/ai-camera/

* 12MP sensor Sony IMX500
* Video modes:
  * 4056×3040 @ 10fps
  * 2028×1520 @ 30fps

**How to:**

https://www.raspberrypi.com/news/how-to-get-started-with-your-raspberry-pi-ai-camera/

## Pi Camera

Camera is connected over the CSI interface on the mainboard.  
Detailed info: https://projects.raspberrypi.org/en/projects/getting-started-with-picamera

You can utilize following script to test out basic functionality.

```sh
$ /home/pi/python_demo/pi_camera_test.py --help
Usage: pi_camera_test.py [OPTIONS]

Options:
  --preview  Shows camera image preview on physical connection only.
  --stream   Starts a server with camera stream
```

**Tech. specs**:

* Still images: 8 Mpx (3280x2464)
* Video modes:
  * 1920x1080 @ 30 fps
  * 1280x720 @ 60 fps
  * 640x480 @ 90 fps

## Speaker pHAT

Audio HAT containing amplifier, speaker and LED bar graph for projects requiring audio output.  
Pi Zero form factor.  
Tech. details: https://web.archive.org/web/20210725202304/https://shop.pimoroni.com/products/speaker-phat  
HAT installer: https://github.com/pimoroni/speaker-phat

## Explorer pHAT

HAT to extend Pi with 5V input/output, analog input,  
Pi Zero form factor.  
Installer: https://github.com/pimoroni/explorer-hat  
Documentation: https://github.com/pimoroni/explorer-hat/blob/master/documentation/Function-reference.md
