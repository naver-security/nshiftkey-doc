---
title: Exception Setting
category: Best Practice
order: 6
---

### Exception setting guide

Toothless can be set up in a variety of ways. Let's take a look at the case below to find out how to handle exceptions in various situations.

> You can do exception setting by using security_check.rc. Refer to [here](https://naver-security.github.io/nshiftkey-doc/4-best-practice/customize_settings) for more detail information.

> You can check ingnore list at the left tab.
> ![](../../images/exception.png)
> 

### You write down sensitive information (password, IP address, tokens, etc.) in a specific file (property file, etc.) and you don't want to report it to Toothless.
It is best not to store sensitive information in Github repository. However, when you are forced to hardcode the information, the following exceptions can prevent the issue from being reported:

1. Modify security_check.rc
2. Enter the file name that contains sensitive information at the "ExcludeFile" entry(including path)
3. Perform Toothless scan

![](../../images/exception-excludefile.png)

### When you don't want to duplicate the security issues that Toothless has detected.
Security issues detected by Toothless will continue to be reported until they are resolved. If you are aware of the issue and you no longer want to receive a report before you make any modifications, you can prevent the issue from being reported through the following exception handling.

### When you do not want to detect the Toothless in the future, you do not need to modify it internally.
As you review the security issues that Toothless has detected, you may decide that those issues do not need to be fixed. The following exception handling can prevent the issue from being reported:

1. Peform Toothless scan
2. Move to "Checks" tab
3. Press "ignore this" button of specific issue
4. Find ignored issue at the ignore list tab

### When a security issue detected by Toothless is false-alarm.
Security issues detected by Toothless may be false-alarm. In this case, the following exception handling prevents the issue from being reported:

1. Peform Toothless scan
2. Move to "Checks" tab
3. Press "ignore this" button of specific issue
4. Find ignored issue at the ignore list tab

### When a security issue detected by Toothless is false-alarm.
Security issues detected by Toothless may be false-alarm. In this case, the following exception handling prevents the issue from being reported:

1. Peform Toothless scan
2. Move to "Checks" tab
3. Press "ignore this" button of specific issue
4. Find ignored issue at the ignore list tab

### When you want to get a report on only issues that have a big impact.
If too many minor security issues are detected in the repository you manage, managing security issues can be difficult. You can use the following exception handling to ensure that only security issues with significant impact are reported:

1. Modify security_check.rc
2. Enter "1" of "2" at the "ReportLevel" entry
3. Perform Toothless scan

![](../../images/exception-reportlevel.png)

### When you want to exclude the Test folder from the detection list.
Typically, test files have data for testing, which can report unwanted security issues. In this case, all files in the test folder can be excluded from detection through the following exception handling:

1. Modify security_check.rc
2. Enter folder name at the "ExcludeDir" entry
3. Perform Toothless scan

![](../../images/exception-excludedir.png)

### When you do not want Toothless to report on a particular detection rule.
Toothless has a large number of detection rules defined and reports on all issues that apply to that rule. The following exception handling lets you avoid reporting issues that correspond to specific rules:
> You can see all rules at [here](https://naver-security.github.io/nshiftkey-doc/1-static-analysis/check_rule).

1. Modify security_check.rc
2. Enter rule name at the "ExcludeCheckRule" entry
3. Perform Toothless scan

![](../../images/exception-excludecheckrule.png)

