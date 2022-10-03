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

### Sandbox

Sandboxing is an important Operating System feature on smartphones (and computers too, but to a lesser degree). Instead of allowing an user application to talk to any other applications or use any system/hardware resources by default, a _sandboxed_ app (or system component) is **by default denied access to resources and outside communication**. Sandboxed components could not affect other parts of the system. A sandboxed component is like a machine that is fully enclosed in a safe.

However, programs do sometimes need system resources to properly function. For instance, a voice recorder app needs read access to the microphone in order to do its job. Thus, different "holes" needs to be punched on the safe in order to allow communication to the outside world. The "holes" represent the legitimate channels of interaction allowed by the sandbox. The permission system on iOS and Android can be seen as high-level abstractions of the holes. When the user gives permission to an app, the system essentially opens a hole on the app's enclosing safe.

The sandbox is usually imposed on user applications and some system components that is in direct contact with user applications or can process untrusted input. The sandbox is enforced by a combination of low-level kernel functionalities. When user applications tries to access forbidden resources, one of the following few things can happen:

* System prompts the user to decide whether to allow access, such as files, camera, microphone.
* System denies the application, the application receives an error.
* System determines that some resource really shouldn't be accessed by any user application, and if the application is accessing those resources, it is probably for some nefarious purpose, thus kills (forcibly stop executing) the application.
* System determines that some resource really shouldn't be accessed by any user application, and the fact that this resource is now being accessed means something nefarious might already be happening, thus it is best to stop the system entirely and reboot, technically referred to as a _kernel panic_.

If the sandbox leaves an unintional hole or a hole can be cracked open by the application, this amounts to a vulnerability. System vendors put in a lot of effort prevent this kind of "sandbox escape" vulnerabilities. Sandbox escape vulnerabilities are rare these days and require highly technical skills to find one.
