# Firmware update from SD-card

RockChip SoC based devices support firmware updates by booting from a specially prepared SD-card. The official way requires a Windows-based application from RockChip ("Create Upgrade Disk Tool", aka "SD Firmware Tool"), and a suitable device boot loader file. Using them, I've prepared such an SD-card for you.

[`DX160FirmwareUpdater.zip`](https://github.com/Lurker00/DX160-Firmware-Add-on/releases/download/DX160FirmwareUpdater/DX160FirmwareUpdater.zip) archive contains ready to use SD-card image file with 4GB partition, to update firmware on iBasso DX160.

## Prepare bootable SD-card
You may use any SD-card with capacity of 4GB or more.

**WARNING:** writing the SD-card image file erases all the data on the card! To restore the SD-card for normal use, please use [SD Memory Card Formatter](https://www.sdcard.org/downloads/formatter_4/), available for MacOS and Windows.

You need to unzip the downloaded archive ([`DX160FirmwareUpdater.zip`](https://github.com/Lurker00/DX160-Firmware-Add-on/releases/download/DX160FirmwareUpdater/DX160FirmwareUpdater.zip)) and write the `DX160FirmwareUpdater.img` file directly to SD-card. Under Windows, [Win32 Disk Imager](https://sourceforge.net/projects/win32diskimager/) can be used. Under Linux and MacOS, [Etcher](https://en.wikipedia.org/wiki/Etcher_(software)) GUI application performs the task (see [below](#an-instruction-for-macos-users) for example). Experienced users may use [`dd` command](https://en.wikipedia.org/wiki/Dd_(Unix)) from console, though great caution is required!

If all went right way, you should have SD-card labeled as `DX160UPDATE`, with the following content:
* `sd_boot_config.config`
* `sdupdate.img`
* `rksdfw.tag`

`sdupdate.img` is empty (0 bytes), and it is the placeholder for the real firmware update image file.

## Update firmware

**WARNING:** Firmware update from bootable SD card is performed only when DX160 is not connected to a power supply or USB port. Charge it before starting firmware update!

You need firmware update image file. My firmware releases to use with SD-card contain compatible `sdupdate.img`.

1. Copy `sdupdate.img` to the prepared bootable SD-card, confirming to overwrite existing file.
2. Safely remove (unmount) SD-card from the computer.
3. Disconnect DX160 from a charger or USB port (if it is connected).
4. If your DX160 boots to Mango, switch it to boot to Android.
5. Turn DX160 off.
6. Insert SD-card into DX160.
7. Turn DX160 on.

In a few seconds it should start updating the firmware. At the end, it will prompt you to remove the SD-card from the slot, and will continue update, then erase storages and boot the device.

## Useful notes

You may keep several firmware images on the bootable SD-card under different file names. Only the one named `sdupdate.img` is used for the firmware update.

## An instruction for MacOS users

Please refer to [DX200 instruction](https://github.com/Lurker00/DX200-Firmware-Add-on/blob/master/FirmwareUpdater/README.md) for more information and hints.
