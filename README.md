# ih8sn-Oneplus7pro
>Custom config of ih8sn for OP7 pro, made with keys from lastest ota update.
-Note am not responsible for any damage you can do to your device by not following the guide properly or flashing wrong files. If you have any issue after installation i wont be providing suppport.


Note: **adb** and **usb debbuging with root** are **required** for procedure.

#How to install:
-------------------------------------------------------------------------------------------------------------------------
1:Download **repo**

2:**Extract** repo

3:**Open cmd** in folder which **contains** extracted **repo** (ih8sn, push.sh, folder named "etc")

4:**paste in** to **command** line shell and execute (you can either one by one or all at once)
>adb wait-for-device root  
>adb wait-for-device remount
>adb wait-for-device push etc/60-ih8sn.sh /system/addon.d/
>adb wait-for-device push ih8sn /system/bin/
>adb wait-for-device push etc/ih8sn.rc /system/etc/init/
>adb wait-for-device push etc/ih8sn.conf /system/etc/
>adb reboot

5: **Delete**: google play, google framework services **data and chache**

6: Enjoy!

Proof of work
----------------------------------------------------------------------------------------------------------------------------
![IMG_20230527_065348](https://github.com/N3kowarriorCZenchilada/ih8sn-Oneplus7pro/assets/118403968/8f083b8a-fd2a-45c9-8378-7bad03d7b61c)
