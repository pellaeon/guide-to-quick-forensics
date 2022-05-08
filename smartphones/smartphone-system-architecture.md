# Smartphone System Architecture

Smartphones are basically small handheld computers, the major architectural distinction from computers are:

* Systems being more locked down:
  * Non-customizable bootloaders
* Addition of special purpose co-processors
  * Secure enclave
  * Baseband
  * Image-processing
  * AI acceleration

### Co-processors

Co-processors are processors used only for a particular purpose other than the system. The co-processors helps the main _application processor_ to handle certain tasks, thus have to communicate with it. Co-processors often run their own embedded operating system and application and could not be directly controlled by the user. Co-processors often has privileged access to system resources and user data, so they are sometimes targets of more sophisticated exploitations. Due to the locked-down nature, it is difficult to audit or obtain forensic data from co-processors. For the purpose of this guide, you will only need to know that:

* Co-processors can be exploited
* Co-processor exploits are sophisticated and uncommon

The rest of this guide will thus focus on the softwares running on the application processor.

### Operating System

Smartphone operating systems differ from computer operating systems in that they implement more controls and isolation between different system components and applications, so that a compromised component could not easily affect the whole system.

![](https://developer.android.com/guide/platform/images/android-stack\_2x.png)

It is possible for attackers to exploit kernel vulnerabilities, however these vulnerabilities are quite rare and usually requires sophisticated techniques to exploit.

### System Applications

System applications may contain vulnerabilities. Once exploited, they can cause greater harm than exploiting user applications, because they usually have more privilege to change the underlying system. One common example is the built-in browser, which is often exploited.

### User Applications

User applications are least privileged. However, if the permissions are granted, they can access sensitive user information, so they can still cause great harm. They can also sometimes trick or exploit the underlying system to gain more control.
