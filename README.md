# BChecks

Welcome to the official BChecks repository from PortSwigger. This repo contains a collection of custom scan checks written in our BChecks language, developed by both PortSwigger and the community with 🧡

BChecks can be imported and used in both Burp Suite Professional and Burp Suite DAST. To write and test your own BChecks, we recommend using Burp Suite Professional, which includes a built-in editor with syntax highlighting and testing tools.

>💡 This repository only contains scan checks written in our custom BChecks language. For checks written in Java, see [custom scan checks in the Bambdas repository](https://github.com/PortSwigger/bambdas/tree/main/CustomScanChecks).

## Resources

### Importing BChecks:
- [Importing custom scan checks](https://portswigger.net/burp/documentation/desktop/extend-burp/custom-scan-checks/importing) (Burp Suite Professional)
- [Adding BChecks to Burp Suite DAST](https://portswigger.net/burp/documentation/dast/user-guide/extensions/adding-extensions#adding-bchecks-to-burp-suite-dast)

### Using BChecks in scans:
  - [Adding custom scan checks to scans](https://portswigger.net/burp/documentation/desktop/running-scans/custom-checks) (Burp Suite Professional)
  - [Scanning with extensions in Burp Suite DAST](https://portswigger.net/burp/documentation/dast/user-guide/scanning-webapps-and-apis/site-settings/scanning-with-extensions)

### Creating BChecks:
If you use Burp Suite Professional, you can write your own BChecks with full editor support:

- [Custom scan checks documentation](https://portswigger.net/burp/documentation/desktop/extend-burp/custom-scan-checks) – Detailed information on creating, testing, and managing both Java-based and BCheck-based scan checks (Burp Suite Professional).
- [Definition reference](https://portswigger.net/burp/documentation/scanner/bchecks/bcheck-definition-reference) – The keywords available when writing a BCheck.
- [Worked examples](https://portswigger.net/burp/documentation/scanner/bchecks/worked-examples) – Example BCheck definitions that correspond to real-world use cases.
- [BCheck v2-beta language](https://youtu.be/lR04_eN4Uuo) – Video overview of functionality available in the BCheck language.

### See BChecks in action:
- [Burp Suite Shorts | BChecks](https://www.youtube.com/watch?v=NaiQMJk4nus) – A quick video introduction to BChecks.
- [Supporting Sprocket Security's offensive security testing with BChecks](https://portswigger.net/blog/supporting-sprocket-securitys-offensive-security-testing-with-bchecks-from-burp-suite)
- [The top 10 community-created BChecks, so far ...](https://portswigger.net/blog/the-top-10-community-created-bchecks-so-far)

## Community submissions
BChecks are a community-driven effort and as such we encourage you to share your own BChecks and improve upon the existing ones.

To learn about the process of contributing to the repository, see [Contributing](https://github.com/PortSwigger/BChecks/blob/main/CONTRIBUTING.md).

## BChecks

### Examples
We've put together some example BChecks, to help you get started:
* Blind SSRF via out-of-band detection
* Exposed git directory
* Leaked AWS Tokens
* Log4Shell via out-of-band detection
* Server Side Prototype Pollution
* Suspicious Input Transformation

[/examples](/examples/)

### Vulnerabilities CVEd
The following BChecks look for specific vulnerabilities which have a CVE:

[/vulnerabilities-CVEd](/vulnerabilities-CVEd/)

### Vulnerability classes
These BChecks look for specific vulnerability classes as opposed to discrete vulnerabilities:

[/vulnerability-classes](/vulnerability-classes/)

### Other
You can see other BChecks that have been created by the community, doing wonderful things that we didn't imagine:

[/other](/other/)

### Archive
You can see archived BChecks that have been preserved for users with older versions of Burp Suite:

[/archived](/archived/)

## Disclaimer
BChecks are written and maintained by third-party users of Burp. We review the pull requests for new community-created scripts before they are added to this repository. However, PortSwigger Web Security makes no warranty about their quality or usefulness for any particular purpose.
