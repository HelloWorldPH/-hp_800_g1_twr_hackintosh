# HP EliteDesk 800 G1 TWR Hackintosh - OpenCore 0.9.1 v1.0.0
The HP EliteDesk 800 G1 TWR is a desktop PC that can be used for hackintoshing with OpenCore 0.9.1. This guide is based on the OpenCore Vanilla Desktop Guide for Haswell, which you should read carefully to understand the process also this EFU is not properly made or maintained. However, my goal is to help you avoid errors you might encounter during the installation process.

# You can comment here if you want help.
https://www.reddit.com/r/hackintosh/comments/12o79rc/hp_elitedesk_g1_800_twr_need_help_with_dortania/?utm_source=share&utm_medium=web2x&context=3

# WARNING: This EFI is not properly made or maintained! 
## v1.0 Issue

| About this MaC |
|:-----------:|
|![](/image.png)|
## Specs
* Intel Core i5-4570 CPU
* Intel Graphics 4600 GPU (iGPU)
* 4GB DDR3 RAM (upgradeable)
* 500GB HDD (replaceable)
* Realtek ALC221 audio
* OpenCore bootloader 0.9.1
## What is working
* macOS Monterey and Big Sur
* Ethernet
* Dual-boot macOS / Windows 10
## What is not working
* Sleep
* Audio

## Video graphics (iGPU)
##About the iGPU and GPU##
The iGPU Intel Graphics 4600 is not working, and you have only 4GB of RAM. You can use an AMD RX 570 GPU instead to improve graphics performance. However, XFX AMD RX 570 GPU may not work. You can use the dGPU platform-id if you want to use your dedicated GPU.

## Installation
Generate SSDTs using SSDTIME and copy them to the ACPI folder.
Replace the EFI folder with the one provided in this guide.
Edit config.plist to enter new serials, UUID, etc.
Use the default desktop platform-id (0x0d220003) for iGPU or dGPU platform-id for dedicated GPU.
## BIOS setup 
Upgrade to the latest BIOS version and make sure VT-d is disabled. Set SATA emulation to AHCI if not already set.

## USB port mapping
You used USBToolBox.kext and UTBDefault.kext for USB port mapping. These should work on your PC of this model.

## Audio
Audio is not working. Please check the config.plist and audio kexts for any errors.

## Sleep
Sleep is not working. Please check the config.plist and power management settings for any errors.

## Video Graphics (iGPU)
The iGPU Intel Graphics 4600 is not working. You can use an AMD RX 570 GPU instead to improve graphics performance. However, if you want to try fixing the iGPU, you can experiment with different values for the ig-platform-id and device-id in the DeviceProperties section of the config.plist.

# ENJOY! 
The HP EliteDesk 800 G1 TWR is a good option for a hackintosh desktop, and with the right hardware upgrades, it can be a powerful machine.


