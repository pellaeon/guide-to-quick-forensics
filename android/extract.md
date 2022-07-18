# Extract Data for Further Analysis

In this section we introduce a few tools that collects device information or backups that could be sent to experts for analysis.

## Backup to Computer

* Using vendor apps such as Samsung's [Smart Switch](https://www.samsung.com/us/support/answer/ANS00048603/).
* Using generic apps such as [https://github.com/mrrfv/linux-android-backup](https://github.com/mrrfv/linux-android-backup)

## \[obsolete] Note: Set-up ADB USB Debugging

To use Snoopdroid, you need to enable USB debugging in the developers options. Here are the instructions to do so from the [official Android documentation](https://developer.android.com/studio/debug/dev-options#enable) :

* On Android 4.1 and lower, the Developer options screen is available by default.
* On Android 4.2 and higher, you must enable this screen as follows:
  * Open the Settings app.
  * (Only on Android 8.0 or higher) Select System.
  * Scroll to the bottom and select About phone.
  * Scroll to the bottom and tap Build number 7 times.
  * Return to the previous screen to find Developer options near the bottom.

At the top of the Developer options screen, you can toggle the options on and off (figure 1). You probably want to keep this on. When off, most options are disabled except those that don't require communication between the device and your development computer.

Next, you should scroll down a little and enable USB debugging. This allows Android Studio and other SDK tools to recognize your device when connected via USB, so you can use the debugger and other tools.

To test that the USB connection is working, you can use the ADB shell, just run `adb devices` and check if you see a connected device. for instance :

```
> adb devices
List of devices attached
RF2F722NU0C	device
```

You can test that the access is working by running `adb shell`, the phone will then ask you to confirm that the device is allowed to debug the phone.

## [androidqf](https://github.com/botherder/androidqf)

androidqf is an easy-to-use desktop application that collects system and app information and outputs them into a files that could be sent to experts for further analysis. Follow the official instructions to operate.
