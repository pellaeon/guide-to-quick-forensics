# Wireshark

## Prerequisite

Set up network traffic monitoring according to [network.md](../smartphones/network.md "mention").

## Usage

Wireshark is a tool to capture network traffic flowing through a network interface.

During first startup, one has to select the network interface that you wish to monitor on. This should be the network interface acting as the Access Point (AP) to the phone. Note: when unsure about which one, unplug the Wifi adapter, plug it in again, and check `sudo dmesg` for detected interface name.

Once traffic is shown to be flowing through, we can start looking for suspicious activities.

![A sample Wireshark capture when an app starts on the phone.](<../.gitbook/assets/wireshark Screenshot\_20220718\_161819.png>)



## Indicators (What to look for?)

### General

* Suspicious domains, e.g. `goog1e.com`
* Direct connection to an IP without DNS query.
* Periodic connection, e.g. every hour, whenever the device boots
* Persistent connection
* Uncommon TCP and UDP ports
* Connection uncorrelated with user activity, such as when the device screen is off, but seeing a lot of network traffic.

### Targeted Threats

Highly stealthy malware, tends to conceal their traffic with other benign apps.

### Remote Access Trojans (RATs)

RATs generally need to communicate to Command and Control servers (C2 servers or C\&C servers) operated by the attacker. The attacker can issue commands to remotely control the infected device. This should involve a lot of two-way traffic.

### Spyware / stalkerware

These malwares usually does not have C2 servers, but rather just continuously collect and upload user information (such as user activity on the system, location) to collection servers.

### Adware / cryptocurrency miners

This category of software is the least intrusive. Adware usually connects to a lot of different sites to produce clicks on advertisements. Miners use the device's processing power to mine cryptocurrencies, and would usually have to connect to mining pools to give results.

## References

* More information on network traffic analysis: [https://www.rapid7.com/fundamentals/network-traffic-analysis/](https://www.rapid7.com/fundamentals/network-traffic-analysis/)
