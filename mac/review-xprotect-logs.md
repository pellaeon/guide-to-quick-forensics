# Review XProtect Logs

[XProtect](https://book.hacktricks.xyz/macos-hardening/macos-security-and-privilege-escalation/macos-security-protections/macos-gatekeeper#xprotect) is a built-in **anti-malware** feature in macOS. XProtect **checks any application when it's first launched or modified against its database** of known malware and unsafe file types. When you download a file through certain apps, such as Safari, Mail, or Messages, XProtect automatically scans the file. If it matches any known malware in its database, XProtect will **prevent the file from running** and alert you to the threat.

For background system scanning, macOS previously used MRT. Since 2022, a new module [XProtect Remediator](https://eclecticlight.co/2023/06/12/malware-detection-and-remediation-by-xprotect-remediator/) was added to macOS.

To check the scan results of XProtect Remediator, use [XProCheck](https://eclecticlight.co/2022/09/05/xprocheck-a-new-utility-to-inspect-anti-malware-scans/). However, Apple has not published details about Remediator, so the logs may be hard to understand.
