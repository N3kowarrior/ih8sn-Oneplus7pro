# ih8sn-Oneplus7pro
Custom config of ih8sn for OP7 pro.

How to:

1:Download repo

2:Extract repo

3:Open cmd in folder which contains extracted repo (ih8sn, push.sh, folder named "etc"

4:paste in 

adb wait-for-device root 
adb wait-for-device remount
adb wait-for-device push etc/60-ih8sn.sh /system/addon.d/
adb wait-for-device push ih8sn /system/bin/
adb wait-for-device push etc/ih8sn.rc /system/etc/init/
adb wait-for-device push etc/ih8sn.conf /system/etc/
adb reboot

5: Enjoy!




Thanks to:https://forum.xda-developers.com/t/guide-ih8sn-pass-safetynet-without-magisk-root.4450323/
          https://github.com/luk1337/ih8sn


![IMG_20230527_065348](https://github.com/N3kowarriorCZenchilada/ih8sn-Oneplus7pro/assets/118403968/8f083b8a-fd2a-45c9-8378-7bad03d7b61c)
