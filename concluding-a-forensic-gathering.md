# Concluding a Forensic Gathering

To conclude a forensic gathering, you should always:

1. Inform user of the findings
2. Preserve evidences
3. Restore the device to its original state

### Malware infections

If malware infections were found on a device, the usual _Incident Response_ procedure applies:

1. Containment
2. Eradication
3. Recovery
4. Lessons learned / evidence retention

Refer to [NIST Computer Security Incident Handling Guide](https://nvlpubs.nist.gov/nistpubs/specialpublications/nist.sp.800-61r2.pdf) for more information.

The incident response procedure changes a lot depending on situations, to give a few examples:

1. An app that steals the user's contacts were installed and used: decide whether leakage of the user's contacts would put anyone in danger. If not, simply remove the app.
2. A malware that tries to steal other apps' login cookies: change passwords of all login accounts, logout all sessions, login again. If the malware exploit system protections, factory reset the system and install the latest system updates, if the device hardware is out of date, urge user to switch to a new device.
