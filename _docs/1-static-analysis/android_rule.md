---
title: Checklist of Android App
category: SAST
order: 3
---

rule name | description
-- | --
Excessive privilege setting | Unnecessary privileges can lead to decreased user convenience and false detection of vaccines.
Setting up vulnerable protection level | Due to the incorrect setting of protocol level for custom permission, there is a possibility that important activities can be called from external apps.
Activity exposure vulnerability | Setting exported Activity allows other apps to access activity, which allows access to data in the private area of the app.
File-based Cross-Site Scripting | A malicious script can cause XSS to intercept the cookie or access of the local file. Important information of the app may be stolen.
JavaScript Interface Injection | If addJavaScriptInterface is used in webview, it is possible that malicious javascript will load. There is a possibility that can call the method of the object.
Path Traversal | In the contextProvider, where openFile is implemented, there is insufficient verification of the safety of the routing characters (../, ./), so other apps can randomly access the private area of the app, which can leak information.
Plaintext of password  | If the setSavePassword option is true in WebView, the entered password may be stored as a plain sentence in the application's data area, and it can be a risk of exposure.
Webview SSLErrorHandler | Unsecured SSLErrorHandler can result in exposure to MITM.
Unsecured TrustManager | Unsecured TrustManager can result in exposure to MITM.
Unsecure Hostname verifier | Unsecured Hostname Verification can result in exposure to MITM.
Vungle AD SDK vulnerability | Vulnerabilities of Vungle AD SDK allow hackers to proxy network traffic and insert payloads extracted from the Vungle app to launch MITM on the device.
MoPub Ad SDK vulnerability | If you use a version prior to 4.4.0 of the MoPub AD SDK, an attacker can exploit this vulnerability to speculate that there is sensitive data locally. For Android devices that use API 16 or earlier, an attacker can also access local data.
OpenSSL vulnerability | The use of vulnerable OpenSSL allows a middleman attacker to downgrade a vulnerable TLS connection to 512-bit export-grade encryption.<br>(“logjam” and CVE-2015-3194, CVE-2014-0224)
Libpng vulnerability | Using the vulnerable version of the Libpng could allow an attacker to execute malicious code.
GnuTLS vulnerability | Using the vulnerable version of the GnuTLS could allow an attacker to control app remotely by triggering a buffer overflow.
SuperSonic SDK vulnerability | If you use a lower version of the Supersonic SDK than 6.3.5, Javascript files are downloaded over HTTP. This allows attackers to change files via MITM.
Libupnp vulnerability | The vulnerable version of the Libupnp contains a stack buffer overflow vulnerability that could allow attacker to execute arbitrary code on the target device.
Libjpeg-turbo vulnerability | If you use a vulnerable version of the Libjpeg-turbo, attacker can use a maliciously crafted JPEG image to read the app's Heap memory.
Vpon Ad SDK vulnerability | If you use a vulnerable version of the Vpon Ad SDK, attacker can use malicious JavaScript code to access local resources.
Android backup vulnerability | If the Android backup setting is not false, attacker can extract the private data of the app through the ADB.
Source code leakage | Non obfuscated code can be decompiled and there are possibility to expose original code.
Debug flag setting vulnerability | If Debug flag is enabled, an attacker can debug the app to analyze code and steal sensitive information.
Server info leakage | If the dev / Alpha / beta server informations are hard-coded in the source code, there are possibility to expose server information.




