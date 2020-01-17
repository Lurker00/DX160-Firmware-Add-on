# iBasso DX160 firmware add-on by Lurker

## Introduction
Android 8.1 for DX160 protects main partitions with [Verity](https://source.android.com/security/verifiedboot), which makes it tricky for end user to flash custom firmware. [Magisk](https://magiskmanager.com/) allows developers to alter system systemless-ly, i.e. without any direct modification of the protected parts of the firmware image. That's why my modifications for 8.1 are distributed as add-ons: you must have installed and running the original firmware, then you apply (flash over) an add-on. It makes the download smaller and update process faster!

To check the current add-on version in Android mode, go to _Settings_, _About DX160_, _Build number_ at the bottom.

**WARNING:** Add-ons are *not* compatible with encrypted devices!<br />
**WARNING:** Do *not* update Magisk via MagiskManager! It will cause problems!

## How to apply or update the add-on
There are two packages to choose from: either Windows-only (using included AndroidTool), or any platform (using [DX160-bootable SD-card](https://github.com/Lurker00/DX160-Firmware-Add-on/tree/master/FirmwareUpdater)). The ZIP archive with the add-on contains `readme.txt` file with full instruction. Please read and follow it.

For Windows, you should have installed drivers from Rockchip. You can download them [here](https://github.com/Lurker00/DX220-Firmware-Add-on/tree/master/files).

**Note:** Updating an add-on removes additional [Magisk](https://magiskmanager.com/) modules. You'll have to re-install them after the update.

## How to return back to the official firmware
If there is a manual OTA-like update package on the [iBasso web site](http://ibasso.com/down.php), it is enough to install it, then do a factory reset. Instead, you can search the [Releases](https://github.com/Lurker00/DX160-Firmware-Add-on/releases) section for a package for your firmware version, and apply it.

## How to update the official firmware
True OTA does not work with add-on, because the build number is different. You have to return back to the official firmware ([see above](#how-to-return-back-to-the-official-firmware)), then use OTA, or download the manual update from [iBasso web site](http://ibasso.com/down.php) and install it. After that, you can apply the [add-on, compatible with the new firmware version](#history-of-public-releases).

## Changes made
It's up to the end user to decide whether these changes affect sound or not. I believe some of them make sound better, and none of them make sound worse.

### Android
* Google Play Market added.
* Reduced power consumption during music playback and in suspend mode.
* Overall performance increased.
* During music playback, the device is managed to prevent idle state tasks.
* Performance tweak for popular music players (Neutron, UAPP, Tidal, Spotify). Such a tweak is used on Rockchip SoC based devices for benchmark apps, iBasso sets it for its Mango Player.
* Better thermal control.
* A different approach to control brightness at low levels.
* The process of [device registration](https://www.google.com/android/uncertified/) is much simplified (required to make Google Play Services work on uncertified device).
* [Magisk](https://magiskmanager.com/) can be used to install additional modules, and to provide root access.
* [USB Audio application](https://github.com/Lurker00/DX200-USB-Audio-Release/blob/master/README.md), which is also useful for its [System settings](https://github.com/Lurker00/DX200-USB-Audio-Release/blob/master/README.md#system-settings).
* Custom build of [HibyMusic](https://play.google.com/store/apps/details?id=com.hiby.music), which plays bit perfect PCM up to 32/384kHz with no additional efforts, and is fully compatible with [USB Audio application](https://github.com/Lurker00/DX200-USB-Audio-Release/blob/master/README.md) for bit perfect DSD and SACD ISO playback.
* Removed APKPure, CoolAPK, Viper HiFi (to free space for Mango OS).
### Mango OS
* Added Mango OS mode from DX220.

**Note 1**: Mango OS player was taken from DX220, and, as such, is not 100% compatible. The known restrictions and problems are:
* Only first 4 Digital Filter options actually work.
* Only two levels of gain actually work: Medium and High produce the same result.
* Optical Output setting does not work.
* If you put on Pause during PCM playback for more than a minute, resuming playback produces silence. Workaround: push Pause/Play one more time.
* After playing DSD files, PCM files don't produce sound. Workaround: either turn the device off then on, or put on pause for one minute or more and resume playback.

**Note 2**: MagiskManager icon is, actually, a stub injected by Magisk core. It is intended by the developer to help installing full MagiskManager, but I disable it to stop annoying. Should you need [MagiskManager, please install it manually](https://github.com/topjohnwu/Magisk/releases).

## History of public releases
* [**1.26**](https://github.com/Lurker00/DX160-Firmware-Add-on/releases/tag/v1.26) - release for official firmware 1.04.145.
* [**1.25**](https://github.com/Lurker00/DX160-Firmware-Add-on/releases/tag/v1.25) - release for official firmware 1.03.123.
* [**1.24**](https://github.com/Lurker00/DX160-Firmware-Add-on/releases/tag/v1.24) - release for official firmware 1.02.109.
* [**1.23**](https://github.com/Lurker00/DX160-Firmware-Add-on/releases/tag/v1.23) - release for official firmware 1.01.084.
* [**1.22**](https://github.com/Lurker00/DX160-Firmware-Add-on/releases/tag/v1.22) - release for official firmware 1.00.055.
