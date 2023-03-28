---
sidebar_position: 1
---

# Semantic Versioning

Versioning is the process of assigning unique version name to unique states of an application or software. Every application must follow a versioning strategy to ensure the smooth wokring of process.
There are many type of versioning strategies are available:

- Semantic Versioning
- Calendar Versioning
- Sprint-based Versioning

In react native applications, we highly recommend to use the semantic versioning strategy that includes `<major>.<minor>.<patch>[.<build number>]` numbers for ease of accessibility.

| Stage         | Example Version |
| ------------- | --------------- |
| Fisrt Release | 1.0.0           |
| Patch Release | 1.0.1           |
| Minor Release | 1.1.0           |
| Major Release | 2.0.0           |

There is a semver supported package avaiable in npm registry to maintain versioning.
[https://www.npmjs.com/package/semantic-release](https://www.npmjs.com/package/semantic-release)

## Setup

run the below command in root directory

```bash
npx semantic-release-cli setup
```

It will ask some questions and complete the setup process based on the answers.
Its better to write a CI for semantic versioning using this package instead of manual versioning.

## References docs

- [https://semver.org/](https://semver.org/)
