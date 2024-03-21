# Code Repository Scanning With SNYK
## Objectives
This lab's primary focus is scanning the forked code repository with SNYK to discover vulnerabilities and attempt to fix them. They show how common vulnerabilities can be uncovered and rectified before its exploited.
## Skills Learned
+ Vulnerability scanning
+ In-depth knowledge of the Common Vulnerability Scoring System (CVSS)
+ Enhanced knowledge of Common Vulnerability and Exposure (CVE).
+ Vulnerability remediation.
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

### Vul. 1

<img width="903" alt="vul high1" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/828313aa-2d23-40dc-b0a4-0617042a0772">

### Vul. 2

<img width="915" alt="vul hig2" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/b6d547fe-ca17-4f4d-9b4f-0a81844c5905">

### Vul. 3

<img width="811" alt="vul hi3" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/048b6082-872e-4f35-aa98-31889cb079ed">

## Recommended fix
Click the Dockerfile to view recommendations for fixing the discovered vulnerablilty. 

<img width="920" alt="recom fix2" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/f4ab4058-36be-471f-bdbd-60b59c322e31">

From the reccomendation, the base image need needs to br upgraded from node:18.19.1 to node:21.7.0-bookworm-slim.

##
To upgrade the base image, Open the forked repository on GitHub. 

<img width="914" alt="dockfile edi 1png" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/9c3c94e0-15a5-4a09-9d9e-e4bc2306b3be">

##

Click Dockerfile to open and replace the 'node:18.19.1' with 'node:21.7.0-bookworm-slim' by clicking the pencil icon to edit. 
<img width="911" alt="docfile edit 21png" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/4aec650d-eb9b-43f5-835e-31b9756ee0e2">

##

Click Commit changes to update the Dockerfile.

<img width="913" alt="doc ed commit1" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/2e8c4ec3-94a3-42a4-abc2-14e894a96473">
<img width="910" alt="commit final1" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/0eea53bd-c483-4611-b1c8-5972042e0e89">

## Verify fix
To verify update, close and reopen SNYK check the current 

## Old Base image

<img width="920" alt="old image" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/1ef00095-84da-46f3-862c-7402ce92418f">

## New Base Image Update

<img width="915" alt="new update" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/591f4799-b436-4860-b1d2-779396e281d5">

## Verify Vulnerability Fix 
##

The previous version of the Dockerfile base image had one critical severity issue, three high severity issues, one medium sevrity issue and one hundred and sixty-three low severity issues.

<img width="916" alt="old vul" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/98518bf7-79f3-4358-972e-b34df7548178">

##

The update eliminated two of the three high severity vulnerability, eliminated the medium severity vulnerability and one hundred and thirty vulnerabilities out of the one hundred and sixty-three vulnerabilities.

<img width="890" alt="vul new fix" src="https://github.com/richard-acquah/Code-Repository-Scanning-With-SNYK-Lab/assets/136107996/603d9c3f-6e42-4d47-98a1-dd9f4e274576">

## Conclusion
Vulnerability scanning and remediation is an unending cycle of preventive measures put in place to reduce the attack surface of an organization.
