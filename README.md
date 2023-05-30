Certainly! Here's the reformatted version for improved readability:

## ih8sn for Oneplus7pro

Custom config of ih8sn for OP7 Pro, made with keys from the latest OTA update. Please note that I am not responsible for any damage that may occur to your device if you do not follow the guide properly or flash wrong files. If you encounter any issues after installation, I will not be providing support.

### How to install

**Note**: `adb` and USB debugging with root access are required for the procedure.

1. Download the repository.
2. Extract the repository.
3. Open the command prompt in the folder that contains the extracted repository (`ih8sn`, `push.sh`, and the folder named "etc").
4. Paste the following commands into the command line shell and execute them (you can execute them one by one or all at once):

```shell
adb wait-for-device root
adb wait-for-device remount
adb wait-for-device push etc/60-ih8sn.sh /system/addon.d/
adb wait-for-device push ih8sn /system/bin/
adb wait-for-device push etc/ih8sn.rc /system/etc/init/
adb wait-for-device push etc/ih8sn.conf /system/etc/
adb reboot
```

5. Delete data and cache of the following:
   - Google Play
   - Google Framework Services

6. Enjoy!

Please ensure that you have adb and USB debugging with root access enabled before proceeding with the installation. Feel free to reach out if you have any further questions.
