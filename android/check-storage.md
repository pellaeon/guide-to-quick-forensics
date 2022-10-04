# Check Storage

Instead of checking every file on the storage, there are a few shortcuts to check for suspicious files:

1. Download history of the user-preferred browser
2. "Recently used" section in the file manager

## Search for APK Files

Sometimes users are tricked into downloading and installing APK files and the APK files were left in phone storage. By searching for APK files, we might find APK files that were installed in the past.

## Search for Suspicious Files

Less sophisticated malware might leave a trace on the phone by writing files in the internal storage (or SD card).

Look for these kinds of files, and search their path in Google:

* `.log`, `.txt` files: might be log files created by malware or spyware
* Files containing copies or backup of sensitive user information, such as call logs, chat history, or contact lists. These information are usually kept only in app storage (storage area only accessible to an app), unless the user intentionally exports them. So any unintentional exports might be a sign of malware stealing data or apps malfunctioning. These files should be deleted quickly after use because the internal storage is less protected.
* `.so` files: `so` stands for "shared object", which can be understood as an extension to an executable file. Existence of `.so` files might indicate that they were loaded and executed.
