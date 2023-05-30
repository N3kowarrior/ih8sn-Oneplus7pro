# ih8sn-Oneplus7pro
>Custom config of ih8sn for OP7 pro, made with keys from lastest ota update.
>Am not responsible for any damage you can do to your device by not following the guide properly or flashing wrong files. If you have any issue after installation i wont be providing suppport.

#How to install:
-------------------------------------------------------------------------------------------------------------------------
Note: **adb** and **usb debbuging with root** are **required** for procedure.

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

#Create yourself
-------------------------------------------------------------------------------------------------------------------------
1:[Download](https://github.com/luk1337/ih8sn/releases/tag/latest) lastest ih8sn release and extract it.

>aarch64 is armv8

2:**Navigate to system/etc** and **open ih8sn.conf** with your favorite text editor.

3:Paste in:

>BUILD_FINGERPRINT=
>BUILD_DESCRIPTION=
>BUILD_SECURITY_PATCH_DATE=
>BUILD_VERSION_RELEASE=
>BUILD_VERSION_RELEASE_OR_CODENAME=
>MANUFACTURER_NAME=
>PRODUCT_NAME=
>BUILD_TAGS=release-keys
>BUILD_TYPE=user
>DEBUGGABLE=0

4:Download and extract lastest stock ota or full firmware for your device.

5:Navigate to META-INF/com/android/

6:Open metadata with your favorite text editor.

7:Locate line with similair text like this :

>POCO/surya_global/surya:12/RKQ1.211019.001/V14.0.1.0.SJGMIXM:user/release-keys
>Note:Names of variables could vary but you should recognise them easily.

8:After second forward slash is device name so write it on line (in ih8sn.conf)containing: PRODUCT_NAME= .
>PRODUCT_NAME=surya

9:Next to that is number (separeted by double colon) add it to line BUILD_VERSION_RELEASE=  and BUILD_VERSION_RELEASE_OR_CODENAME=.
>BUILD_VERSION_RELEASE=12

10:Paste the whole "POCO/surya_global/surya:12/RKQ1.211019.001/V14.0.1.0.SJGMIXM:user/release-keys" to line BUILD_FINGERPRINT=.
>BUILD_FINGERPRINT=POCO/surya_global/surya:12/RKQ1.211019.001/V14.0.1.0.SJGMIXM:user/release-keys

11:Build description is text after third foward slash.
>BUILD_DESCRIPTION=V14.0.1.0.SJGMIXM

12:Locate BUILD_SECURITY_PATCH_DATE= in manifest and paste date after it to line containing BUILD_SECURITY_PATCH_DATE=.
>BUILD_SECURITY_PATCH_DATE=2023-02-01

13:Now just type name of company which created your smartphone to MANUFACTURER_NAME=.
>MANUFACTURER_NAME=Xiaomi

14:Save ih8sn.conf

15:Continue with installation above from 3 step
