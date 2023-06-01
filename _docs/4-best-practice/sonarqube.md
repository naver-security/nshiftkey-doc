---
title: Using SonarQube
category: Best Practice
order: 7
---

### Using SonarQube
* NShiftKey has a Sonarqube, so you can also check SonarQube's results.
* The version of SonarQube used by NShiftKey : Community Edition (v8.9)

### Matching Severity between SonarQube and NShiftKey
* The Severity Levels of SonarQube and NShiftKey are matched as shown in the table below.

SonarQube | NShiftKey
-- | --
BLOCKER  | HIGH
CRITICAL | HIGH
MAJOR    | MEDIUM
MINOR    | LOW
INFO     | LOW


### Matching result between SonarQube and NShiftKey
* The result(report) of SonarQube and NShiftKey are matched as shown in the table below.

SonarQube | NShiftKey
-- | --
Vulnerabilities | code security check
Bugs | sonarqube - bug
Code smells | sonarqube - code smell


### Default of report level
The default of report level for each type are as follows:

* Vulnerability : ALL (BLOCKER, CRITICAL, MAJOR, MINOR, INFO)
* Bug : only BLOCKER, CRITICAL
* Code smell : only BLOCKER

> Please refer to the link for more information about SonarQube's issue type / report level. [[link]](https://docs.sonarqube.org/latest/user-guide/issues/)

### Changing default of report level
If you want to change default of report level, please refer to this link. [[Customizing Setting]](https://naver.github.io/nshiftkey-doc/4-best-practice/customize_settings/)
