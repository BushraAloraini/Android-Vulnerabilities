# Android-Vulnerabilities

## 1- Android Vulnerabilities Dataset

The dataset includes:
 - Mined Android vulnerabilities from NVD. 
 - Android vulnerabilities analysis over time.
 - Android app vulnerability types analysis.
 - Android app Buffer Error vulnerability analysis.
 
### Mined Android Vulnerabilities from NVD. 
This dataset includes 2,089 Android vulnerability records and 20 fields. 13 fields were mined from NVD, and 7 fields were added to classify given vulnerabilities. 
The following tables describe the dataset fields:

####  NVD Fields
| NVD Fields               | Description
| ----------------------   | ------------------------------------ | 
| CVE-ID                   | CVE Identifier number.
| Original release date    | The date on which the vulnerability was available in the NVD database.
| Last revised date        | The date that the NVD supplied the most recent updates about the vulnerability.
| Source                   | Information source.
| Overview                 | Brief description of the security vulnerability or exposure.
| CVSS v2 Base Score       | The overall CVSS v2 score.
| Impact  Subscore         | Represents the subscores of  Confidentiality Impact (C), Integrity Impact (I), Availability Impact (A).
| Exploitability Subscore  | Represents the subscores of  Access Vector (AV), Access Complexity (AC), Authentication (Au).
| Access Vector            | Measures how remote an attacker can be to exploit a vulnerability.
| Access Complexity        | Measures the complexity of attack required to exploit the vulnerability once an attacker has access to the target system.
| Authentication           | Measures the number of times an attacker must authenticate to a target once the system has been accessed in order to exploit a vulnerability.
| Impact Type              | Clarifies the impact of the vulnerability in terms of Confidentiality, Integrity, Availability.
| Vulnerability Type       | The vulnerability weakness type that follows the Common Weakness Enumeration (CWE). 

#### Added Fields
| Added Fields             |  Description
| ----------------------   |------------------------------------| 
| Software Type            | Indicates whether the the vulnerability is more related to Android OS or Android apps.
| Classification Note      | Provides information about the infected element that helped in classifying.
| Classification Rule      | Refers to the keyword that utilized to classifying.
| Include                  | Refers to whether the record was included or excluded from our study.
| Record Category          | Includes the category that we used to categorize such records. See the table below for more information.
| Record Category URL      | Includes links to locate information that leads to categorization.
| Note                     | Includes some nots about the vulnerability when available.


 #### Record Category
 
| Record Category                      |  Description
| --------------------------------     | ------------------------------------ | 
| Confirmed and patched                | An advisory has been published by the vendor that explains the vulnerability and provides patching information. 
| Reported and patched                 | The vulnerability has been reported to the vendor and patches were released. 
| Proof of concept and patched         | A proof of concept has been demonstrated by the reporter, and it is indicated that the vendor has released patches.
| Confirmed but not patched            | The vulnerability has been confirmed by the vendor, however no patches were provided.
| Proof of concept but not patched     | A proof of concept has been demonstrated by the discoverer, and it is indicated that the vendor has not released patches.
| Not enough information               | In case that the vulnerability report does not include enough information, such as a proof of concept, patching information, or confirming from the vendor
| Large-scale experiment               | The vulnerability was discovered through an automated large scale experiment. 
 
 Note: To show records analyzed in our study, filter "Include" feild to "YES". Then, to show Android apps vulnerabilities, filter "Software Type" to "Android app".


## 2- Ubuntu 64-bit 16.4 vm
The virtual machine includes the source code of the following Android vulnerabilities:
1. CVE-2008-0985
2. CVE-2012-4190
3. CVE-2014-1705
4. CVE-2014-1710
5. CVE-2014-3201
6. CVE-2016-5182
7. CVE-2016-5199
8. CVE-2016-5200
9. CVE-2017-5014

In addition, the vm has the following static analysis tools being installed:
- RATS
- Flawfinder
- Cppcheck
- Clang static analyzer
- Frama-C along with Frama-Clang 
- IKOS

### Usage
To analyze the source code of the above vulnerable apps using the above static analysis tools, execute `run_analysis.sh`  script in SATs directory which is located on the Desktop.

