---
title: Requirement
category: SAST
order: 1
---

### Features

The static analysis module of NShiftKey supports the following features:

- Source code vulnerability scanning
  - Results can be available in the "code security check" tab
- Source code bug scanning
  - Results can be available in the "sonarqube - bug" tab
- Source code code smell scanning
  - Results can be available in the "sonarqube - code smell" tab
- Opensource vulnerability scanning
  - Results can be available in the "open source vulnerability check" tab
- Sensitive data leakage scanning
  - Results can be available in the "sensitive data leakage check" tab

Language-specific support analysis functions are as follows:

Language | Source code | Opensource | Sensitive data
-- | -- | -- | --
Java | O | O | O
Javascript/Typescript | O | O | O
Go | O | O | O
C (C++) | O | O | O
Kotlin | O | O | O
Python | O | O | O
Ruby | O | O | O
Objective C (Swift) | | O | O
Scala | O | O | O
HTML | O | | O
CSS | O | | O


### Trigger condition of Source code vulnerability scanning 

NShiftKey performs a source code vulnerability scanning when PR occurs.

> NShiftKey detects the language of repository through language detection API provided by Github.
Github's API provides a language distribution based on default branch of repository. 
Therefore, some analyses may not be performed if language composition between target branch and default branch is different. ( ex) If default branch is empty, analysis does not proceed even if there are contents in target branch.)

### Language-specific conditions

1. Javascript: Analyze based on ECMAScript5 grammar.
2. Go: Projects must be buildable for precise analysis. Analysis is possible even if it is not built.
3. Scala: Only projects managed by sbt(Simple Build Tool) can be analyzed, and you cannot analyze a project that is not buildable. The supported scalar versions are limited to (2.11.X, 2.12.X, 2.13.X).

### Success or failure of the analysis upon build status

O : available
X : fail
△ : partial available

| Language | Success or failure |
|------|---|
|C/C++|O|
|JAVA|X|
|JavaScript|O|
|TypeScript|O|
|Go|△|
|Kotlin|O|
|Scala|X|
|Objective C (Swift)|O|
|Ruby|O|
|Python|O|
