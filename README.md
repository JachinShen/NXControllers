# Bluetooth Linux Driver for Nintendo Switch Ringcon
This driver is based on https://github.com/mpawlowski7/NXControllers. I learn the ringcon protocol from https://github.com/Yamakaky/joy and add ringcon support.

## Build instructions
### Dependencies 

* Ubuntu and derivatives 
``sudo apt install dkms linux-headers-`uname -r` ``  

### Installation
* `git clone https://github.com/JachinShen/NXControllers`
* `cd nxcontrollers`
* `sudo ./install.sh`

## Usage
* Load module `sudo modprobe hid_nintendo` (or reboot)
* Press pairing button on joycon, quickly insert it into the ringcon and connect via Bluetooth.
* Ringcon flex value is shown in the second value of IMU field, typical /dev/input/js1

## Update
* `git pull`
* `sudo ./update.sh`

## Uninstallation
* Run `sudo ./uninstall.sh` to remove all installed versions of hid-nintendo.
