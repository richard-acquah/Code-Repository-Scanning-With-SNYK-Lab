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

<img width="916" alt="scan rresul1t" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/7e5e91d0-a500-4023-bdd1-11fd919ad2cd">

##
Expand the fgxgm-SecurityCheckSample to view the files. 

<img width="922" alt="dock file1" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/c0a0e8e2-bbd0-4b46-81bc-33083aa9a307">

## Vulnerability Details 
Click the Dockerfile to view details of the vulnerabilities. 

The issues section shows a critical vulnerability known as Integer Overflow with CVSS score of 9.8 on the of 10.

<img width="880" alt="vuln detail criti1" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/fc31b0e8-d9a9-47c0-996c-166fea960a20">

##
The issues section also shows three highe severity vulnerability known as Out-of-bound Write, Resource Exhaustion and Allocation of Resources Without Limits or Throttling with the CVSS score of 7.8, 7.5 and 7.5 respectively.

<img width="903" alt="vul high1" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/828313aa-2d23-40dc-b0a4-0617042a0772">
<img width="915" alt="vul hig2" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/b6d547fe-ca17-4f4d-9b4f-0a81844c5905">
<img width="811" alt="vul hi3" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/048b6082-872e-4f35-aa98-31889cb079ed">

## Recommended fix
Click the Dockerfile to view recommendations for fixing the discovered vulnerablilty. 

<img width="920" alt="recom fix2" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/f4ab4058-36be-471f-bdbd-60b59c322e31">

From the reccomendation, the base image need needs to br upgraded from node:18.19.1 to node:21.7.0-bookworm-slim.

##
To upgrade the base image,

