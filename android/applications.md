# Review Installed Applications

## Application ID

Some malicious applications are presented as legitimate applications, often being a copy of a legitimate application with malicious code added to them. Go to **Settings > Applications**, and click on each application to check its ID at the page bottom.

![](../.gitbook/assets/Screenshot\_20220506-170511\_Settings.png)

The application ID should reflect the app's displayed name, for example, the authentic "Play Store" app's ID is `com.android.vending`, however, there are also [malwares](https://www.tomsguide.com/news/octo-android-malware-can-take-over-your-phone-how-to-protect-yourself) pretending to be the Play Store with ID `com.restthe71`.&#x20;

### Application version

On the same App Info page, the app version is also displayed. One can search the app version on Google to determine whether the version actually exists. If there are lots of search results returned for the version string, then the version probably exists. For example, the above screenshot shows the app com.twitter.android version 9.36.0-release.0 is installed, and searching for "twitter 9.36.0" returns many search results, which indicates that this version is probably legitimate. However, if you see something like "version 100", then the app is probably fake.

## Permissions

Even if fake applications were installed, they still need an important number of Android permissions to be able to monitor your phone remotely, so a first step is to check the list of applications installed and their permissions.

To do that, visit **Settings > Applications**

![](../img/android\_apps1.png)

This menu is showing you a list of all the applications installed. You should visit the page of each of these applications and check for the permissions allowed for them.

The following permissions are specifically suspicious as they are very regularly used by malicious applications :

* Location
* Contacts
* SMS
* Microphone
* Camera
* Call logs
* Phone

![](../img/android\_apps2.png)

It is also interesting to check other parameters about this app, that may or may not be displayed depending on your version of Android :

* Check if the app was installed from the Google Play store : see **App details** or **App details in store**
* Check if the app can modify system settings or have other "Special App Access" : see **Modify system settings** or **Change system settings**. Follow [this guide](https://web.archive.org/web/20221004090852/https://www.techbone.net/android/user-manual/permission-to-modify-system-settings) to open the settings.
* Check if the app is allowed to install other applications : see **Install unknown apps**

## Running Applications

To inspect running apps, follow [this guide](https://web.archive.org/web/20220509061723/https://www.techrepublic.com/article/how-to-view-all-running-services-on-android-11/).

Check unknown running apps by googling their names.

Disable Developer Options after inspecting running apps to prevent leaking information.

