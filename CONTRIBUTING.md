# Contributing

When contributing to this repository, please first feel free to raise a pull request.

Please note that we have a code of conduct. Please follow it in all your interactions with the project.

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

Requirements: Java 17+

In the top level directory of the folder containing your BChecks, run the following command:
```
java -jar BCheckChecker-1.5.jar
```

Verify the output. To do this quickly, check the exit code is 0 for a valid run.

### What it checks for

- Valid syntax.
- Populated metadata fields.
- Use of the .bcheck file extension.
- Inappropriate use of the passive tag.



## Code of Conduct

### Our Pledge

In the interest of fostering an open and welcoming environment, we as
contributors and maintainers pledge to making participation in our project and
our community a harassment-free experience for everyone, regardless of age, body
size, disability, ethnicity, gender identity and expression, level of experience,
nationality, personal appearance, race, religion, or sexual identity and
orientation.

### Our Standards

Examples of behavior that contributes to creating a positive environment
include:

* Using welcoming and inclusive language
* Being respectful of differing viewpoints and experiences
* Gracefully accepting constructive criticism
* Focusing on what is best for the community
* Showing empathy towards other community members

Examples of unacceptable behavior by participants include:

* The use of sexualized language or imagery and unwelcome sexual attention or
advances
* Trolling, insulting/derogatory comments, and personal or political attacks
* Public or private harassment
* Publishing others' private information, such as a physical or electronic
  address, without explicit permission
* Other conduct which could reasonably be considered inappropriate in a
  professional setting

### Our Responsibilities

Project maintainers are responsible for clarifying the standards of acceptable
behavior and are expected to take appropriate and fair corrective action in
response to any instances of unacceptable behavior.

Project maintainers have the right and responsibility to remove, edit, or
reject comments, commits, code, wiki edits, issues, and other contributions
that are not aligned to this Code of Conduct, or to ban temporarily or
permanently any contributor for other behaviors that they deem inappropriate,
threatening, offensive, or harmful.

### Scope

This Code of Conduct applies both within project spaces and in public spaces
when an individual is representing the project or its community. Examples of
representing a project or community include using an official project e-mail
address, posting via an official social media account, or acting as an appointed
representative at an online or offline event. Representation of a project may be
further defined and clarified by project maintainers.

### Enforcement

Instances of abusive, harassing, or otherwise unacceptable behavior may be
reported by contacting the project team via issues. All
complaints will be reviewed and investigated and will result in a response that
is deemed necessary and appropriate to the circumstances. The project team is
obligated to maintain confidentiality with regard to the reporter of an incident.
Further details of specific enforcement policies may be posted separately.

### Attribution

This Code of Conduct is adapted from the [Contributor Covenant][homepage], version 1.4,
available at [http://contributor-covenant.org/version/1/4][version]

[homepage]: http://contributor-covenant.org
[version]: http://contributor-covenant.org/version/1/4/
