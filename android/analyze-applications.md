# Analyze Applications

## Scanner apps

Some apps automatically check the apps installed on the system (to see if they are known to be malicious).

* [Koodous Antivirus](https://play.google.com/store/apps/details?id=com.koodous.android)
* [Lookout](https://play.google.com/store/apps/details?id=com.lookout)

These scanner apps work by extracting and uploading the APKs to their own platform. Some device information and potentially other personal information might be uploaded as well, one should check the platforms' privacy policy before installing and scanning with those apps.

## Extract Application Bundles (APKs)

Some tools require you to extract the APK files manually and upload them. Below are some tools that can extract APKs.

* [Apk Extractor](https://play.google.com/store/apps/details?id=com.ext.ui\&hl=zh\_TW)
* [Apk Extractor (open source)](https://f-droid.org/packages/axp.tool.apkextractor/)

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

