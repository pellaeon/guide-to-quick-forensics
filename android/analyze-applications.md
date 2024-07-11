# Analyze Applications

## Scanner and antivirus apps

Some apps automatically check the apps installed on the system (to see if they are known to be malicious).

* [Koodous Antivirus](https://play.google.com/store/apps/details?id=com.koodous.android)
* [Lookout](https://play.google.com/store/apps/details?id=com.lookout)

These scanner apps work by extracting and uploading the APKs installed on the system to their own platform and comparing the APKs to known malwares. Some device information and potentially other personal information might be uploaded as well, one should check the platforms' privacy policy before installing and scanning with those apps.

Alternatively, there is an open-source antivirus application [Hypatia](https://github.com/Divested-Mobile/Hypatia), which utilizes signature databases from ClamAV, ESET and the [targeted threats list made by brotherder](https://github.com/botherder/targetedthreats).&#x20;

These scanner and antivirus apps can only see what other apps are installed, and cannot inspect deep into the operating system, because they themselves are sandboxed. However, medium to highly sophisticated malwares will embed themselves into the system without being shown as an app. These scanner and antivirus apps' knowledge of malwares also depends on their databases, whose sources often come from their enterprise customers. Thus, the scanner apps usually can only find malwares that package themselves as apps (which are usually medium to low sophistication), and are already known. However, these scanners can be installed and operated very easily, therefore they are still useful as a first-line test.

After finishing the check, uninstall the scanner apps to prevent further data collection.

## Extract Application Bundles (APKs)

Some tools require you to extract the APK files manually and upload them. Below are some tools that can extract APKs.

* [Apk Extractor](https://play.google.com/store/apps/details?id=com.ext.ui\&hl=zh\_TW)
* [Apk Extractor (open source, last update in 2018)](https://f-droid.org/packages/axp.tool.apkextractor/)
* [Kanade](https://github.com/alexrintt/kanade) (open source, last update in 2022)

Once an APK is extracted, one can also calculate its file hash (MD5 or SHA), and search for the hash using sites like VirusTotal.com .

## Online tools

### [Exodus Privacy](https://reports.exodus-privacy.eu.org/en/)

Exodus Privacy is a tool for privacy. It can analyze apps and list trackers contained in an app.

### [Hybrid-analysis.com](https://www.hybrid-analysis.com/)

Hybrid-analysis allows you to upload an APK file to scan. It checks the APK using various antivirus software and VirusTotal.

### [MobSF](https://github.com/MobSF/Mobile-Security-Framework-MobSF)

MobSF decompiles the application and analyze its contents, listing things like URLs, static files, and Activities. These can then be used to motivate further analysis.

There is a online version of MobSF available at [https://mobsf.live](https://mobsf.live).

You can also [host](https://mobsf.github.io/docs/#/installation) MobSF yourself, or use free hosting services like [Play with Docker](https://labs.play-with-docker.com/) to host a private MobSF instance. Play with Docker provides 4 hours of session time.

## Other tools

There are also other online analysis tools. The ones listed below are not specialized in APK.

* [https://cuckoo.cert.ee/](https://cuckoo.cert.ee/)
* [https://app.any.run/](https://app.any.run/)
* [https://www.virustotal.com/](https://www.virustotal.com/)

## Interpreting Analysis Results

The tools will produce a lot of technical information about the app, interpreting them would require technical understanding of how mobile apps work (such as: what are _content providers, services, activity_). However partial analysis could be achieved by simply checking if the files, URLs, IP addresses contained in the app is already known to be malicious.
