# iBasso DX160 firmware add-on by Lurker

## Introduction
Android 8.1 for DX160 protects main partitions with [Verity](https://source.android.com/security/verifiedboot), which makes it tricky for end user to flash custom firmware. [Magisk](https://magiskmanager.com/) allows developers to alter system systemless-ly, i.e. without any direct modification of the protected parts of the firmware image. That's why my modifications for 8.1 are distributed as add-ons: you must have installed and running the original firmware, then you apply (flash over) an add-on. It makes the download smaller and update process faster!

To check the current add-on version in Android mode, go to _Settings_, _About DX160_, _Build number_ at the bottom.

**WARNING:** Add-ons are *not* compatible with encrypted devices!
**WARNING:** Do *not* update Magisk via MagiskManager! It will cause problems!

## How to apply or update the add-on
There are two packages to choose from: either Windows-only (using included AndroidTool), or any platform (using [DX160-bootable SD-card](https://github.com/Lurker00/DX160-Firmware-Add-on/tree/master/FirmwareUpdater)). The ZIP archive with the add-on contains `readme.txt` file with full instruction. Please read and follow it.

For Windows, you should have installed drivers from Rockchip. You can download them [here](https://github.com/Lurker00/DX220-Firmware-Add-on/tree/master/files).

**Note:** Updating an add-on removes additional [Magisk](https://magiskmanager.com/) modules. You'll have to re-install them after the update.

## How to return back to the official firmware
After iBasso released OTA-like update, it will be enough to re-apply any official firmware update, then do a factory reset. Until then, I provide packages to revert back to the official firmware the same way as you flashed the add-on.

## How to update the official firmware
True OTA does not work with add-on, because the build number is different. You need to download the update from [iBasso site](http://ibasso.com/down.php), put it to SD-card or Internal storage, and start manual upgrade. Then you may install an add-on compatible with the new firmware version, if any.

## Changes made
### Android
* Google Play Store added.
* [Magisk](https://magiskmanager.com/) can be used to install additional modules, and to provide root access.
* [USB Audio application](https://github.com/Lurker00/DX200-USB-Audio-Release/blob/master/README.md), which is also useful for its [System settings](https://github.com/Lurker00/DX200-USB-Audio-Release/blob/master/README.md#system-settings).
* Custom build of [HibyMusic](https://play.google.com/store/apps/details?id=com.hiby.music), which plays bit perfect PCM up to 32/384kHz with no additional efforts, and fully compatible with [USB Audio application](https://github.com/Lurker00/DX200-USB-Audio-Release/blob/master/README.md) for bit perfect DSD and SACD ISO playback.
* 126MHz CPU frequency added (216MHz is officially lowest), which is enough for most tasks.
* Overall performance increased.
* During music playback, the device is managed to prevent idle state tasks.
* Better thermal control, to prevent overheating.
* A different approach to control brightness at low levels.
* Less power consumption in suspend mode.
* The process of [device registration](https://www.google.com/android/uncertified/) is much simplified (required to make Google Play Services work on uncertified device).
### Mango
* Added Mango mode from DX220.

## History of public releases
* [**1.22**](https://github.com/Lurker00/DX160-Firmware-Add-on/releases/tag/v1.22) - release for official firmware 1.00.055.
