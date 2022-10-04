# Check if the Phone is under Android Device Policy

The [Device Administrators](https://www.android.com/enterprise/management/) feature allows an organization (usually companies employing the device owner) to remotely administer the device, such as to remotely wipe data when the device is stolen. However, this remote functionality can also be abused by an attacker to steal user data.

Go to Settings > Security > Device Administrators and make sure that none is enabled.

If the [Android Device Policy app](https://play.google.com/store/apps/details?id=com.google.android.apps.work.clouddpc\&gl=US) is installed and enabled in the above setting, make sure the Google Workspace domain that is managing the device is trusted. To do this, check signed-in Google accounts on the device (if they are under trusted Google Workspace domain).
