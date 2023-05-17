---
title: Differential Analysis
category: Best Practice
order: 4
---
### Analyze Modified Files Only
- NShiftKey analyzes all source codes in the Repository by default.
- You can set to analyze only modified codes in Pull Request via security_check.rc setting.
> Please refer to DifferentialAnalysis section of here[(link)](https://naver-security.github.io/nshiftkey-doc/4-best-practice/customize_settings/).

### Supported Languages
- Differential Analysis functionality is supported for all of the following languages: However, C/C++, JAVA, and Scala output only vulnerabilities detected in modified files after full scan internally.
- The application status by language is as follows.
  - Unsupported language acts as full scan.

| Language | Support status |
------|------
| C/C++ | O (full scan) |
| JavaScript | O |
| TypeScript | O |
| Java | O (full scan) |
| Go | O |
| Python | O |
| Ruby | O |
| Objective-C | O |
| Swift | O |
| Kotlin | O |
| Scala | O (full scan) |

### Differential Analysis inoperative Environment
- If there is no history of inspection (if it is the first inspection)
- If there are more than 100 modified files
- If request for analysis via PR is made 30 days after analysis has been performed
- Open source analysis does not support Differences Analysis analysis.
   - Because open source analysis is process that determines whether a vulnerable library is used or not, it cannot be scanned partially.

### Differential Analysis in Multi-language Repository
- The behavior of Differential Analysis depends on the language configuration of the Repository.

| language composition | code security check | open source vulnerability check | sensitive data leakage check | 
------|------|------|------
| Unsupported languages | Unsupported |  Unsupported | Unsupported |
| Supported languages | Supported | Unsupported | Supported |
| Supported languages + Unsupported languages | Partially supported | Unsupported | Supported |

#### In case of a Mix of Supported and Unsupported Languages
##### code security check
- Internally, the supported language operates as Differential Analysis, and the unsupported language operates as full scan.
- For example, if Python and C are simultaneously present in a repository, the Python code acts as Differential Analysis, but the C code acts as full scan.
- The actual results screen shows differential analysis applied in all languages, regardless of the functional behavior within Differential Analysis.
