---
description: >-
  This page serves as my note for setting up network traffic monitoring on
  Linux.
---

# Note: Monitoring Network Traffic on Linux

## Configure WiFi Sharing

Using KDE

1. Plug-in a wifi adapter that supports AP mode.
2. Right click on the Network icon on the taskbar. Click _Configure Network Connections._
3. Click _Add,_ select _Wi-Fi (Shared)._
4. Under Wi-Fi tab, set:
   1. SSID: whatever you want
   2. Limit Device: select the adapter you just plugged in.
   3. Wireless Security: configure a WPA2 Personal password
   4. IPv4: _Method_: _Share with other computers_
5. Choose a connection name (basically the network profile name)
6. Save
7. Left click on the Network icon, click Connect on the connection name you just created.
8. Now the AP should be started and you should see it from other devices the SSID you just configured.

## Configure Redirection to Intercepting Proxy

For mobile forensics, it is usually not necessary to intercept SSL traffic, because to intercept SSL traffic one would typically have to configure a self-signed SSL certificate authority (CA) for the mobile device, however most apps would not trust user-imported SSL CA. To make apps trust the self-signed CA would require rooting the Android device, which is not recommended because when conducting forensics one should not alter the subject device.
