# Contributing

When contributing to this repository, please first feel free to raise a pull request.

Please note that we have a code of conduct. Please follow it in all your interactions with the project.

> 🔎 This repository is for BCheck-based Bambda scripts. If you want to contribute Java-based scan check scripts, please head to the Bambdas repository instead.

## Pull Request Process

1. Place your BCheck in the appropriate folder. For example, BChecks referencing CVEs should be placed in the `vulnerabilities-CVEd` folder.
2. Include a description of the BCheck you are adding in the pull request.
3. Make sure the BCheck follows our [Submission Guidelines](#submission-guidelines).
4. Engage with any comments and feedback given in the review.
5. If your pull request contains multiple BChecks, please be aware that you may be asked to split your PR. This would happen if some BChecks require further feedback while others are ready to merge.

## Submission Guidelines

1. Where possible, please ONLY link to the primary research.
2. Please make sure all metadata fields are completed.
3. Please make sure the BCheck is syntactically valid (see [BCheckChecker](#bcheckchecker)).
4. Please make sure the BCheck is formatted correctly.
   - Indentation is four spaces, not tabs.
5. Please make sure the BCheck is optimized.
   - For  single items please use the define block, not the run for each block.
   - Avoid excessive nested if blocks. Instead, try to combine them into a single if statement.
   - Use appropriate conditionals.
     - Avoid unnecessary matching.
     - Perform simple matches first. For example: status code before headers before regex match on body.
   - Avoid unnecessary or repeat requests.
   - Try to perform any checks on the base response before issuing any requests or payloads.
6. Please attempt to minimize false positives.
   - For bugs in particular frameworks, attempt to fingerprint the framework before reporting the issue.
     - Look for specific markers in a response.
     - Look for specific behavior.
   - Make sure your payload has triggered the behavior.
     - Try to issue a control request. For example, if detecting a change in status code for a particular payload, try to issue a similar invalid payload and verify that only the payload triggers the expected response.
7. Please avoid excessive use of comments.
   - Use of appropriately named variables should mean that your BCheck is self-documenting.

## BCheckChecker

This is a standalone Java program that is run as part of the pull request process. It performs basic validation against a BCheck, and can also be run manually.

### How to run manually

Requirements: Java 21+

In the top level directory of the folder containing your BChecks, run the following command:
```
java -jar BCheckChecker-1.9.jar
```

Verify the output. To do this quickly, check the exit code is 0 for a valid run.

### What it checks for

- Valid syntax.
- Populated metadata fields.
- Use of the .bcheck file extension.
- Inappropriate use of the passive tag.

## Code of Conduct
Please ensure that you are familar with and respect our [code of conduct](https://github.com/PortSwigger/BChecks/blob/main/CODE_OF_CONDUCT.md).
