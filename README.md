# Code Repository Scanning With SNYK
## Objectives
This lab's primary focus is scanning the forked code repository with SNYK to discover vulnerabilities and attempt to fix them. They show how common vulnerabilities can be uncovered and rectified before its exploited.
## Skills Learned
+ Vulnerability scanning
+ In-depth knowledge of the Common Vulnerability Scoring System (CVSS)
+ Enhanced knowledge of Common Vulnerability and Exposure (CVE).
## Resources/ Tools / Utilities
+ Windows 10 22H2 device with internet access.
+ Github account with a forked repository.
+ SNYK
## Steps:
This lab uses a repository forked from https://github.com/ibm-developer-skills-network/fgxgm-SecurityCheckSample.git

<img width="1404" alt="forked to my page1" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/cfa638a3-d455-455e-9227-a919ae711a77">

##
To add the forked repository to SNYK, log in via https://app.snyk.io/login and log in with a GitHub account. 
Authorize SNYK to access Public repositories on GitHub.

<img width="1645" alt="snyk login1" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/633a06a6-ad31-4aab-8aa2-cb1a416e3b3c">

##
After authorization to access GitHub, the SNYK dashboard is displayed. To scan the repository, click Add Projects and select GitHub.

<img width="1874" alt="select gith1" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/01ff54c7-eede-42fa-aab2-9cfcd9cfba9d">

##
Select the forked repository to scan and click Add selected repositories. The forked repository starts importing to SNYK projects.

<img width="1139" alt="choose repo to scan --fgxgm1" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/86b0f97b-f12b-490a-95a9-77bc2fe1846a">
<img width="767" alt="importing project1" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/b18acab9-9cb8-4443-9afa-16d9c2236deb">


##
 Once the scan is complete, the result of the scan is displayed.
