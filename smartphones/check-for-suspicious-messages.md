# Check for Suspicious Messages

Messages containing links are a common attack vector.

![A message containing a link that infects the target with Cytrox Predator malware. Source: Citizen Lab](https://citizenlab.ca/wp-content/uploads/2021/12/Fig-7.png)

Links could be sent from any instant messaging apps or SMS. There are a few kinds of malicious links:

| Link target                                                             | Attacker goal                                                       | Sophistication | Mitigation                                      |
| ----------------------------------------------------------------------- | ------------------------------------------------------------------- | -------------- | ----------------------------------------------- |
| Phishing website, such as a webpage that looks like Google's login page | Trick user into entering personal data or passwords                 | Low            | Check webpage domain names and SSL certificates |
| App download                                                            | Convince user to download and install the app                       | Low            | Don't install apps outside of app stores        |
| Webpage containing web exploits, such as XSS (Cross Site Scripting)     | Steal online session cookies, or operate the currently open session | Medium         | Don't click on links sent by unknown people     |
| Webpage containing a browser exploit                                    | Exploit browser or app vulnerability                                | High           | Don't click on links sent by unknown people     |

### Saving messages

1. Copy the entire message including the link to clipboard
2. Alternatively, save a screenshot containing the full text
3. If you can, archive the link using the [Wayback Machine](https://web.archive.org/)

### Checking links

Simply Google search the link, or paste the link to sites like VirusTotal.
