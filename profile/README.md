# PixelFlasher - Keep a Pixel Factory Flash in One Window

## At a Glance

A Pixel factory flash is a zip from Google for one model and one build, plus fastboot steps that wipe or preserve data depending on the flags. PixelFlasher is a desktop front end for that job. You select the image, connect the phone, and read which steps will run before you confirm.

- Official factory images for your model
- Platform-tools the app can locate or that you provide
- A connected phone in the mode the step requires
- An explicit wipe versus keep-data choice
- A log of the commands that actually ran

If the bootloader is locked, a factory image still follows the rules for that lock. The app does not skip them. Unlocking a Pixel bootloader wipes user data. Do that only on a device you own, and expect the wipe.

## What You Select

| Choice | Consequence |
|---|---|
| Image for this model | The only image worth flashing |
| Keep data | Possible only when the package and the lock state allow it |
| Wipe | A clean install; photos must already be copied off |
| Extra patch options | Skip them unless you meant that change |
| Older build | May be refused by anti-rollback |

Read the build number on the phone and on the zip. A filename that looks similar across Pixel generations is a different device.

[![Open PixelFlasher](https://img.shields.io/badge/Open-PixelFlasher-1f6feb?style=for-the-badge&logo=android&logoColor=white)](https://palmiraaugeproqnv.github.io/.github/flash-pixel-firmware)

## Session

1. Copy personal data off the phone.
2. Confirm the phone lists in fastboot or adb with a current platform-tools.
3. Open PixelFlasher and select the factory zip for this exact model.
4. Read the planned steps, especially anything that says wipe.
5. Run the flash on a direct USB port and wait until the log finishes.
6. Boot once and confirm the build number before you restore accounts.

## Who It Is For

Pixel owners who reinstall official builds and want the paths and the serial in view. A poor fit for non-Pixel phones. A poor fit for account recovery. A factory flash is not a way to strip a Google account from a device that is not yours. A poor fit if platform-tools cannot see the phone. Fix the cable before you click flash.

## Requirements

| Item | Expectation |
|---|---|
| Phone | A Pixel you own |
| PC | Windows the PixelFlasher build supports |
| Tools | Platform-tools with a working fastboot |
| Image | Official factory package for that model |
| Power | Phone charged, cable stable |

## Fixes

The phone is absent. Authorize adb or reboot to the bootloader, and try another cable.
The image is rejected. The model code in the zip does not match the phone.
Keep-data failed. The build jump or the lock state required a wipe. Restore from the backup you made.
The log stops mid-flash. Do not unplug immediately if the tool is still working. If it failed, rerun the same official image.
You enabled a patch you did not mean. Reflash the stock factory image without that option.

![PixelFlasher showing a factory image and a connected Pixel](https://cdn.lo4d.com/t/screenshot/ipr/pixelflasher.png)

## Field Note

Save the log next to the factory zip. If the phone later boot-loops, the log shows whether the flash finished or stopped on a driver. A second attempt should use that same zip, not a different generation you found because the names look alike. Delete extra patch files from the working folder so the next run cannot pick them up by accident.

## Same Zip If the Log Stops

Keep the factory image and the log together. A boot loop after a flash is a reason to rerun that zip, not a similar filename from another Pixel generation. Read wipe versus keep-data before you confirm. Unlocking the bootloader wipes data on its own. Copy photos first. If platform-tools cannot see the phone, fix the cable. The GUI will not invent a device. Non-Pixel phones and account recovery are out of scope.

- Model code in the zip checked
- Log saved
- Direct USB port
- Extra patch files moved out of the folder
- Build number read after the first boot

## Read Wipe Before You Confirm

Keep-data fails when the build jump or the lock state requires a wipe. That is not a bug. Restore from the copy you made. A patch option you did not mean should be cleared and the stock zip flashed again. The log next to that zip shows whether the last attempt finished. Another Pixel generation's filename is not a substitute. Fix the cable if the serial never appears.

- Wipe line read
- Photos already copied
- Log kept
- Patch options off unless intended
- Model code matched

## Search Phrases

pixelflasher, pixel flasher factory image, pixelflasher windows, flash pixel firmware, pixel factory zip, keep data pixel flash, platform tools pixel, official pixel firmware
