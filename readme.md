# Mouse Jiggler
## Overview
Are you using a locked-down machine and being driven to madness by the number of times you have to log in every day? Are you trying to stop your screen saver from triggering? You could buy a Mouse Jiggler, or if you have a Raspberry Pi Pico, you could make one quickly and simply.

## Requirements
- This guide assumes you are using Windows 10
- Raspberry Pi Pico
- USB to Micros-USB cable

## Build
The steps to get jiggler running on your Pico are as follows:
1. Install MicroPython
2. Install Circuit Python for Pico
3. Install adafruit_hid
4. Copy the script to the Pico

---

## 1. Install MicroPython

1. Connect the micro USB end of the cable to your Pico
2. Hold down the BOOTSEL button on your Pico
3. Connect the USB end of the cable to your computer
4. Pico will boot and a mass storage drive named RPI-RP2 will appear on your computer

## 2. Install Circuit Python for Pico

1. Get the latest version of Circuit Python from [here](https://circuitpython.org/board/raspberry_pi_pico/)
2. Download the UF2 file and copy it into the root folder (RPI-RP2) of your Pico
3. Your Pico will restart and after a few seconds a new drive will appear called CIRCUITPY

## 3. Install adafruit_hid

1. Clone this repository to your local machine : 
https://github.com/adafruit/Adafruit_CircuitPython_HID
2. Copy the folder named adafruit_hid within the cloned repository into the root of the Pico.

## 4. Copy the python code file to the Pico

1. Copy code.py to the root folder of your Pico replacing the default copy.py file that is there.  Note that Micropython expects the root module to be named code.py.
2. Your Pico will restart - if you're using the supplied script without modification, the LED on the Pico should flash after 5 seconds, and then once every 5 minutes thereafter (when it jiggles the mouse). If you missed the restart, unplug the USB and reconnect it (don't hold down the BOOTSEL button)
