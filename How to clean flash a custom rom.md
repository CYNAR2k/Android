# How to clean flash a custom rom

## Drivers

- First of all i use the following method related to drivers.
https://forum.xda-developers.com/t/official-tool-windows-adb-fastboot-and-drivers-15-seconds-adb-installer-v1-4-3.2588979/

- I download this first: https://forum.xda-developers.com/attachment.php?attachmentid=4623157&d=1540039037

- Then to avoid any issues with my device not being found in fastboot mode i do this: https://forum.xda-developers.com/attachments/howto_driver-zip.2480396/

- And then i download the latest adb drivers: https://dl.google.com/android/repository/platform-tools-latest-windows.zip 
On this folder is where i do all my adb/fastboot stuff. I just open a CMD window on this folder and execute everything here to avoid any problems.

## Bootloader unlock

## Clean flash from MIUI to custom ROM

- If you are already on MIUI all you have to do is download a custom recovery for your phone & drop it on the platform tools folder and rename it to recovery.

- Download your custom ROM and drop it inside of the platform tools folder.

- Reboot to fastboot. How? Turn off your phone. Now press power + volume down.

- Now that you are in fastboot open CMD inside of platform tools and type: fastboot flash recovery recovery.img

- Now type: fastboot reboot recovery. If it doesn't work press power button + volume up, eventually it will reboot to your custom recovery.

- Now that you are on the custom recovery, factory reset & then wipe data and type yes to confirm. Reboot to recovery via the custom recovery you are using. Now the way I do it is to adb sideload my custom rom. Your custom recovery probably have a way to go into adb sideload, once you manage to get there, open a CMD on platform tools and type: adb sideload "your custom rom name here.zip".

- Factory reset & wipe data again. Reboot to recovery & then reboot to system. (Some will say this it's too much but for me it works great and fixed some problems I had before)

- Done, enjoy your custom ROM.
