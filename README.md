## Cloning Raspberry Pi OS to SD card
- Download and install Raspberry Pi Imager: https://www.raspberrypi.org/downloads/
- Choose Raspberry Pi OS (32-bit), 1.1GB download
- Choose SD card
- Choose Write


## Setup with PI
- Pi initial setup, select lang, network and get updates


## Increase GPU memory
- Open terminal (black icon on menu bar) and enter these commands:
- `sudo nano /boot/config.txt`
- add this to last line: `gpu_mem=512`
- ctrl + X, enter to save file


## Cloning repository and installing rpisurv
- Open terminal (black icon on menu bar) and enter these commands:
- `mkdir rpisurv`
- `cd rpisurv`
- `git init`
- `git remote add origin https://github.com/case112/rpisurv-cust`
- `git pull origin master`
- `sudo ./install.sh`
- `sudo reboot`

## Get new updates from git
- hold letter `q` on keyboard to exit feed
- `cd rpisurv`
- `git pull remote origin`
- `sudo ./install.sh`
- `sudo reboot`


## Update conf file
- hold letter `q` on keyboard to exit feed
- `sudo nano rpisurv/surveillance/conf/surveillance.yml`
- make changes, ctrl + X, enter to save file
- `cd rpisurv`
- `sudo ./install.sh`
- `sudo reboot`


