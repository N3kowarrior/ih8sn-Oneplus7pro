How to install

Note: ADB and USB debugging with root access are required for the procedure.

    Download the repository.

    Extract the repository.

    Open the command prompt in the folder that contains the extracted repository (ih8sn, push.sh, folder named "etc").

    Paste the following commands into the command prompt and execute them (you can execute them one by one or all at once):

    shell

adb wait-for-device root
adb wait-for-device remount
adb wait-for-device push etc/60-ih8sn.sh /system/addon.d/
adb wait-for-device push ih8sn /system/bin/
adb wait-for-device push etc/ih8sn.rc /system/etc/init/
adb wait-for-device push etc/ih8sn.conf /system/etc/
adb reboot

Delete: Google Play, Google Framework Services data, and cache.

Enjoy!



Create yourself

    Download the latest ih8sn release from here and extract it.

        Note: If you have an aarch64 architecture, it is armv8.

    Navigate to system/etc and open ih8sn.conf with your favorite text editor.

    Paste the following lines into ih8sn.conf:
BUILD_FINGERPRINT=
BUILD_DESCRIPTION=
BUILD_SECURITY_PATCH_DATE=
BUILD_VERSION_RELEASE=
BUILD_VERSION_RELEASE_OR_CODENAME=
MANUFACTURER_NAME=
PRODUCT_NAME=
BUILD_TAGS=release-keys
BUILD_TYPE=user
DEBUGGABLE=0
Download and extract the latest stock OTA or full firmware for your device.

Navigate to META-INF/com/android/.

Open metadata with your favorite text editor.

Locate the line with similar text like this:
"POCO/surya_global/surya:12/RKQ1.211019.001/V14.0.1.0.SJGMIXM:user/release-keys"
"Note: Names of variables could vary, but you should recognize them easily."

After the second forward slash is the device name. Write it on the line (in ih8sn.conf) containing PRODUCT_NAME=.

    PRODUCT_NAME=surya

Next to that is a number (separated by double colon). Add it to the lines BUILD_VERSION_RELEASE= and BUILD_VERSION_RELEASE_OR_CODENAME=.
BUILD_VERSION_RELEASE=12

Paste the whole "POCO/surya_global/surya:12/RKQ1.211019.001/V14.0.1.0.SJGMIXM:user/release-keys" to the line BUILD_FINGERPRINT=.
BUILD_FINGERPRINT=POCO/surya_global/surya:12/RKQ1.211019.001/V14.0.1.0.SJGMIXM:user/release-keys
Build description is the text after the third forward slash.

    BUILD_DESCRIPTION=V14.0.1.0.SJGMIXM

Locate BUILD_SECURITY_PATCH_DATE= in the manifest and paste the date after it to the line containing BUILD_SECURITY_PATCH_DATE=.

    BUILD_SECURITY_PATCH_DATE=2023-02-01

Now, just type the name of the company that created your smartphone to MANUFACTURER_NAME=.

    MANUFACTURER_NAME=Xiaomi

Save ih8sn.conf.

Continue with the installation starting from step 3 above.

#Search words ignore this
>Oneplus Oneplus 7pro hide root root ih8sn google certification ctf 
