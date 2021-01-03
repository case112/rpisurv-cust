# Option 1 - Clone RPi image from existing SD card
## Making a copy of the image on your computer
- Remove SD card from RPi that you wish to clone and insert it into your computer
- Follow the first part of the instructions (link below)
- Instructions: https://computers.tutsplus.com/articles/how-to-clone-your-raspberry-pi-sd-cards-with-windows--mac-59294
- Then follow the second part to restore a SD card from a clone

# Option 2 - Start from scratch and create a new RPi image
## Cloning Raspberry Pi OS to SD card
- Download and install Raspberry Pi Imager: https://www.raspberrypi.org/downloads/
- Choose Raspberry Pi OS (32-bit), 1.1GB download
- Choose SD card
- Choose Write

## Setup with PI
- Pi initial setup, select lang, network and get updates

## Increase GPU memory
- open terminal (black icon on menu bar) and enter these commands:
- `sudo nano /boot/config.txt`
- add this to last line: `gpu_mem=512`
- ctrl + X, enter to save file

## Cloning repository and installing rpisurv
- open terminal (black icon on menu bar) and enter these commands:
- `mkdir rpisurv`
- `cd rpisurv`
- `git init`
- `git remote add origin https://github.com/case112/rpisurv-cust`
- `git pull origin master`
- `sudo ./install.sh`
- `sudo reboot`


# Other commands
## Make changes in configuration file - change camera feeds
- make sure there is internet connection
- hold letter `q` on keyboard to exit feed
- `sudo nano rpisurv/surveillance/conf/surveillance.yml`
- make changes, ctrl + X, enter to save file
- `cd rpisurv`
- `sudo ./install.sh`
- `sudo reboot`

## Get new updates from git
- make sure there is internet connection
- hold letter `q` on keyboard to exit feed
- `cd rpisurv`
- `git pull remote origin`
- `sudo ./install.sh`
- `sudo reboot`

## Open GUI
- hold letter `q` on keyboard to exit feed
- `startx`

## Shut down
- hold letter `q` on keyboard to exit feed
- `sudo halt`


