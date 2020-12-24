# Vivo Android Debloater

Clean your Vivo bloated device without root! The list of bloatware app are from [Technastic](https://technastic.com/vivo-bloatware-preinstalled-apps-list/).

## Requirement

- **ADB**
- Python3
- A bloated Vivo or any android device

## Debloating

1. Clone this repo:
   ```bash
   git clone https://github.com/webdevsuperfast/android-debloater && cd android-debloater
   ```
2. Connect device with `adb` and test with:
   ```bash
   adb devices
   ```
3. Run 
   ```bash
   adb shell pm list packages > pkg.list
   ```
5. Open **pkg.list** file and add a hyphen(-) to the bloat apps.
   
   For eg:
   Change
   `package:com.bloat.bs`
   to
   `-package:com.bloat.bs`
6. Save **pkg.list** and run:
   ```bash
   python debloater.py
   ```

## Reinstalling Apps

1. Connect device with `adb` and test with:
   ```bash
   adb devices
   ```
2. Run
   ```bash
   adb shell cmd package install-existing com.android.packagename ## Replace packagename to the package name you wish to restore.
   ```
## Known Issues

1. Inability to add Google Account after removing GMail(com.google.android.gm) & Gmail Services(com.google.android.gms).

## Useful links

* [Bloatware App List](https://technastic.com/vivo-bloatware-preinstalled-apps-list/)
* [XDA - Uninstall Carrier OEM Bloatware](https://www.xda-developers.com/uninstall-carrier-oem-bloatware-without-root-access/)
* [XDA - Install Back Uninstalled Apps](https://forum.xda-developers.com/t/how-to-get-install-back-uninstalled-apps-apks-with-adb.3894235/)