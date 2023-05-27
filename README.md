# ih8sn-Oneplus7pro
Custom config of ih8sn for OP7 pro.

How to:

1:Download repo

2:Extract repo

3:Open cmd in folder which contains extracted repo

4:paste in 

adb wait-for-device root 
adb wait-for-device remount
adb wait-for-device push etc/60-ih8sn.sh /system/addon.d/
adb wait-for-device push ih8sn /system/bin/
adb wait-for-device push etc/ih8sn.rc /system/etc/init/
adb wait-for-device push etc/ih8sn.conf /system/etc/
adb reboot

5: Enjoy!
