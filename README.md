# Rpisurv 2 - Raspberry pi surveillance an RPI IP Camera Monitor

## Setting up RaspiOS and SDcard with macOS
- diskutil list
- diskutil unmountDisk /dev/diskN
- sudo dd bs=1m if=path_of_your_image.img of=/dev/rdiskN; sync
- sudo diskutil eject /dev/rdiskN


## Setup with PI
- Startup setup, select lang, network etc
- if already up to date skip these: sudo apt update, sudo apt full-upgrade

## Increase GPU memory
- Open terminal (black icon on menu bar)
- sudo nano /boot/config.txt
- add this to last line: gpu_mem=512
- ctrl + X, enter to save file


## Cloning repository and installing rpisurv
- Open terminal (black icon on menu bar)
- mkdir rpisurv
- cd rpisurv
- git init
- git remote add origin https://github.com/case112/rpisurv-cust
- git pull origin master
- sudo ./install.sh
- sudo reboot

## Make modifications @ conf file
- hold letter 'q' on keyboard
- sudo nano /etc/rpisurv.conf

## Get new updates from git
- cd rpisurv
- git pull remote origin
- sudo ./install.sh
- sudo reboot





Extras: `git clone https://github.com/SvenVD/rpisurv`

