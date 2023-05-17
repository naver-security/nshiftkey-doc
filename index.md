---
title: Introduction to NShiftKey
---

NShiftKey is an Github-based DevSecOps support system developed by Naver Security. NShiftKey automates security analysis without slowing DevOps workflows.

> [What is DevSecOps?](https://www.redhat.com/ko/topics/devops/what-is-devsecops) DevSecOps = DevOps security built-in


### DevOps of Naver

The picture below shows the DevOps workflow of Naver. The goal of NShiftKey is to provide automated security analysis to the areas marked by the DevOps environment.

![](/images/naver_devops.png)

### DevSecOps with NShiftKey

NShiftKey operates based on Github. By minimizing developers' involvement and automating settings, development workflows are not affected.

NShiftKey provides two features: 
- Code SAST(Static application security testing): Find the security vulnerabilities in the program without building the code
- Opensource Analysis: Analyze known security vulnerabilities of libraries which are using in the program. (like CVE)

![](/images/devsecops.png)


### Cautions

NShiftKey can help maintain robust security, but it cannot replace the security assessment process. Therefore, even if a project uses NShiftKey, security assessment is mandatory.


### Official Channel

> [https://github.com/naver-security/nshiftkey-doc/issues](https://github.com/naver-security/nshiftkey-doc/issues)

We are running an official NShiftKey channel. We provide you with information about NShiftKey, including guides and release notes, and we welcome your enquiries and proposals.
