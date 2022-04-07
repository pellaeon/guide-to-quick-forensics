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
* Co-processor exploits are sophiscated and uncommon
