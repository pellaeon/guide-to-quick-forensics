# Check if the Phone is Rooted

## What is "root"?

"root" is a system superuser account on all Android systems (actually all UNIX-like operating systems, including Linux, macOS and iOS). The root user is allowed to do anything on the system. Usually, only a few (but not all) system processes run as root. User applications never run as root, but in less privileged (normal) accounts.

Sometimes, users want to customize the system in a way not allowed for normal accounts, such as to remove the built-in apps installed by the vendor ("bloatware") to release storage space. In this case, users need to "root" their system, which means to obtain direct control of the "root" account on the system.

Rooting generally involves:

1. Unlock the device bootloader.
2. Flash a custom "recovery operating system" (often just called "recovery"), which is a minimal operating system living on a separate storage partition. The original purpose of recovery is to install system updates.
3. Using the custom recovery, flash (install) the root bundle.

In the rooting process, important system security features are disabled (such as bootloader unlock). A rooted system also adds more attack vector to the system.

## Look for Root-Related Applications

When a phone is rooted, the process often involves installing an application to manage root access, most of the time [Magisk](https://github.com/topjohnwu/Magisk) (or [SuperSU](http://www.supersu.com/) on old versions of Android). One first step is to check if the Magisk application is installed. You can check directly for the icon in your main menu, or go to **Settings > Applications** and search the application.

![](../img/supersu.png)

## Check with Root Verifier

Root Verifier is an [open source](https://github.com/abcdjdj/RootVerifier-APP) application that check if an Android Phone is rooted through different techniques. You can install it from the [Google Play Store](https://play.google.com/store/apps/details?id=com.abcdjdj.rootverifier) or from the [F-Droid repository](https://f-droid.org/packages/com.abcdjdj.rootverifier/).

Once installed, you can launch the application. The interface is really simple, you just need to click on "CHECK" and wait for the result.

![](../img/rootverifier1.png) ![](../img/rootverifier2.png)
