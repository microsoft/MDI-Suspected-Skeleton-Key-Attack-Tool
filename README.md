# Microsoft Defender for Identity - Aorato Skeleton Key Malware Remote DC Scanner

[**Click here to download the tool**](https://github.com/microsoft/MDI-Suspected-Skeleton-Key-Attack-Tool/releases/)

Remotely scans for the existence of the Skeleton Key Malware (http://www.secureworks.com/cyber-threat-intelligence/threats/skeleton-key-malware-analysis/)

The script works as follows:

Verifies whether the Domain Functional Level (DFL) of current domain supports AES (>= 2008)
Finds an AES supporting client account (msds-supportedencryptiontypes >= 8)
Sends a Kerberos AS-REQ to all DCs with only AES E-type supported (Using python code based on PyKek https://github.com/bidord/pykek, see PyKek-original-README.md)
If AS-REQ fails due to AES encryption not supported, then there’s a good chance the DC is infected
 

Prerequisites: Python 2.7 needs to be installed

Usage: powershell ./AoratoSkeletonScan.ps1

Verified on the following platforms:

| OS  | Is Verified |
| :------------- | :------------- |
| Windows 10  | No  |
| Windows Server 2012  | No  |
| Windows Server 2012 R2  | No  |
| Windows Server 2008 R2  | No  |
| Windows Server 2008  | No  |
| Windows Server 2003  | No  |
| Windows Server 2016  | No  |
| Windows 8  | Yes  |
| Windows 7  | No  |
| Windows Vista  | No  |
| Windows XP  | No  |
| Windows 2000  | No  |

[**Click here to download the tool**](https://github.com/microsoft/MDI-Suspected-Skeleton-Key-Attack-Tool/releases/)
