# Check if Developer Options is Enabled

If [Developer Options](https://developer.android.com/studio/debug/dev-options) is enabled, one can control a phone using the Android Debug Bridge (ADB) over USB, or over Wifi if Wifi Debugging is enabled. ADB would also allow attackers to drop executables onto the phone in `/data/local/tmp` and execute it as the `shell` system user.

Unless the phone under check is used for Android App development, **it is not normal to enable Developer Options.** You should find out the reason why and when the user enabled it.

If Developer Options is enabled, you should:

* Check whether there are apps installed via ADB, if so, analyze these apps.
* Check for suspicious files under `/data/local/tmp`

Once you have determined that no malware was installed using ADB, Developer Options should be disabled.

For high risk users, checking the two items above is not sufficient, since there are many other ways ADB could be used to infect a device, and it might also be possible that after the infection the attacker cleared out their traces. Thus, we recommend factory wiping the device before continue using it.
