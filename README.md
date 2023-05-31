## ih8sn for Oneplus7pro

Custom config of ih8sn for OP7 Pro, made with keys from the latest OTA update. Please note that I am not responsible for any damage that may occur to your device if you do not follow the guide properly or flash wrong files. If you encounter any issues after installation, I will not be providing support.

### Recovery installation

**Note**: `adb`, USB debugging enabled and Lineage OS/Custom recovery are required for the procedure.

1. [Download](https://github.com/N3kowarriorCZenchilada/ih8sn-Oneplus7pro/releases/tag/main) the release.
2. Plug your device to your computer.
3. Open command line and type in and execute:
```shell
adb reboot recovery
```

4. Click Apply Update.
5. Paste in cmd:
```shell
adb sideload path/to/zip
```
7. Confirm installation of not signed update.
8. Reboot your device.
9. Delete data and cache of the following:
   - Google Play
   - Google Framework Services

10. Enjoy!

### Manual installation

**Note**: `adb` and USB debugging with root access are required for the procedure.

1. [Download](https://github.com/N3kowarriorCZenchilada/ih8sn-Oneplus7pro/releases/tag/main) the release.
2. Extract the release.
3. Open the command prompt in the folder that contains the extracted repository (`ih8sn`, `push.sh`, and the folder named "etc").
4.Paste the following commands into the command line shell and execute them (you can execute them one by one or all at once):

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

Please ensure that you have adb and USB debugging with root access enabled before proceeding with the installation.

Sure! Here's the reformatted version for better readability:

## Create for yourself:

1. [Download](https://github.com/luk1337/ih8sn/releases/tag/latest) the latest ih8sn release and extract it.
   > Note: aarch64 stands for Armv8.

2. Navigate to `system/etc` and open `ih8sn.conf` with your favorite text editor.

3.Remove file contents and paste the following lines into `ih8sn.conf`:
   ```
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
   ```

4. Download and extract the latest stock OTA or full firmware for your device.

5. Navigate to `META-INF/com/android/`.

6. Open `metadata` with your favorite text editor.

7. Locate a line with a similar text like this:
   ```
   POCO/surya_global/surya:12/RKQ1.211019.001/V14.0.1.0.SJGMIXM:user/release-keys
   ```
   > Note: Names of variables could vary, but you should recognize them easily.

8. After the second forward slash is the device name. Write it on the line (in `ih8sn.conf`) containing `PRODUCT_NAME=`.
   ```
   PRODUCT_NAME=surya
   ```

9. Next to the device name is a number (separated by double colon). Add it to the lines `BUILD_VERSION_RELEASE=` and `BUILD_VERSION_RELEASE_OR_CODENAME=`.
   ```
   BUILD_VERSION_RELEASE=12
   ```

10. Paste the whole "POCO/surya_global/surya:12/RKQ1.211019.001/V14.0.1.0.SJGMIXM:user/release-keys" to the line `BUILD_FINGERPRINT=`.
    ```
    BUILD_FINGERPRINT=POCO/surya_global/surya:12/RKQ1.211019.001/V14.0.1.0.SJGMIXM:user/release-keys
    ```

11. The build description is the text after the third forward slash.
    ```
    BUILD_DESCRIPTION=V14.0.1.0.SJGMIXM
    ```

12. Locate `BUILD_SECURITY_PATCH_DATE=` in the manifest and paste the date after it to the line containing `BUILD_SECURITY_PATCH_DATE=`.
    ```
    BUILD_SECURITY_PATCH_DATE=2023-02-01
    ```

13. Type the name of the company that created your smartphone in `MANUFACTURER_NAME=`.
    ```
    MANUFACTURER_NAME=Xiaomi
    ```

14. Save `ih8sn.conf`.

15. Continue with the installation starting from step 3 above.

## Related/Sources
   [Ih8sn](https://github.com/luk1337/ih8sn)
   
   [xda: ih8sn - Pass SafetyNet without Magisk/Root](https://forum.xda-developers.com/t/guide-ih8sn-pass-safetynet-without-magisk-root.4450323/)
   
   [xda: How to Pass SafetyNet on Android](https://www.xda-developers.com/how-to-pass-safetynet-android/?newsletter_popup=1)


Keywords 
>this is for search engine
>SafetyNet bypass, Device signature spoofing, Anti-SafetyNet, Safetynet workaround, non-root, no root, Device fingerprint >manipulation, Safetynet evasion, Spoofing Safetynet checks, Safetynet bypass for custom ROMs, Lineage OS, Oneplus, >Oneplus 7 pro, Create your own, Safetynet API manipulation, Spoofing device information, Safetynet bypass without root, >Spoofing device information without root, Safetynet bypass for non-rooted custom ROMs, Safetynet evasion on non-rooted Android devices
