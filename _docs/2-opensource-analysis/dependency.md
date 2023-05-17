---
title: Dependency and vulnerability
category: Opensource Analysis
order: 2
---

### Library dependency, CVE, CPE

The use of opensource libraries is essential for software development.
NShiftKey periodically receives known vulnerability list information from NIST(National Institute of Standards and Technology) for analyzing opensource library vulnerabilities.
The list of known vulnerabilities is called Common Vulnerabilities (CVE) and is being distributed with Common Platform Enumeration (CPE).
CPE is a structured naming scheme for information technology systems, software, and packages.

### CVE

NShiftKey periodically receives CVE information from NIST(National Institute of Standards and Technology). In addition, NShiftKey periodically receives vulnerability information related to Javascript or NodeJS from RetireJS (https://github.com/RetireJS/retire.js).

> For the RetireJS data, sometimes there is no CVE information. In this case, NShiftKey creates and identifies an ID in the form like RET-XXXX-XXXX.


### Impact score, Severity

In general, security vulnerabilities are given severity through numerical or level. NShiftKey provides a severity based on Common Vulnability Scoring System (CVSS V2). Impact score is marked from 0 to 10 and Severity has low, medium, and high values.
(https://www.first.org/cvss/v2/guide)


### How to check library in NShiftKey

NShiftKey periodically receives standard CPE data and analyzes that for obtaining the names and versions of libraries. Sometimes it is difficult to analyze CVE information of library if name of particular library differs from the name indicated in the CPE.

> If you are using a library where vulnerabilities exist but do not have a list in the analysis report, inform us to help improve system accuracy.


### Transitive Dependency

When you import the libraries of your project, those libraries themselves have the dependencies which are called as the Transitive dependency.
NShiftKey does not perform vulnerability scan for these transitive dependencies. This is because it is common for each library to be self-managed.
