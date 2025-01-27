# PassTester

### Usage
PassTester is a tool for finding user passwords that are most vulnerable to dictionary attacks. The aim is to prompt the users concerned to choose a more secure password.

First, the tool extracts the NTDS database from the Active Directory (requires domain admin rights). This can be done from any machine in the domain.

Once this has been done, the script retrieves the NTLM hash of each user in the Active Directory and compares it with a database containing, to date, almost 9 billion leaked passwords. No information such as the domain name, user name, etc. is transmitted, only the NTLM hash is provided.

The script will pause for 10 minutes every 1000 hashes so as not to reach the limit set by the ntlm.p website.

If this is carried out as part of an audit, it is recommended not to carry out this second phase from the company's public IP address in order to limit any risk of reverse resolution.

Be sure to delete the NTDS extraction files at the end of each run to limit any risk of data compromise.

### Exemple
![image](https://github.com/Elymaro/PassTester/blob/main/assets/Screenshot.png)

### Thanks
Thanks to [Lars KARLSLUND](https://www.linkedin.com/in/lkarlslund/) for his projet https://ntlm.pw

### Disclaimer
PassTester is intended exclusively for research, education, and authorized testing. Its purpose is to assist professionals and researchers in identifying vulnerabilities and enhancing system security.

Users must secure explicit, mutual consent from all parties involved before utilizing this tool on any system, network, or digital environment, as unauthorized activities can lead to serious legal consequences. Users are responsible for adhering to all applicable laws and regulations related to cybersecurity and digital access.

The creator of PassTester disclaims liability for any misuse or illicit use of the tool and is not responsible for any resulting damages or losses.
