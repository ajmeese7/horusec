<a href="https://github.com/ZupIT/horusec/releases"><img src="https://img.shields.io/github/v/tag/ZupIT/horusec?color=green&label=Version"/></a>
<a href="https://github.com/ZupIT/horusec/actions?query=branch%3Amaster+"><img src="https://img.shields.io/github/workflow/status/ZupIT/horusec/e2e/master?label=Build"/></a>
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

<p></p>
<p></p>
<p align="center" margin="20 0"><a href="https://horusec.io/"><img src="assets/horusec_logo.png" alt="logo_header" width="65%" style="max-width:100%;"/></a></p>
<p></p>
<p></p>

# Table of Contents

 * [What is Horusec](#what-is-horusec)
 * [Project roadmap](#project-roadmap)
 * [Getting started](#getting-started)
 * [Installing](#installing)
 * [Usage](#usage)
      * [Requirements for usage horusec-cli](#requirements-for-usage-horusec-cli)
 * [Usage locally](#usage-locally)
      * [Default Development account](#default-development-account)
      * [Requirements for use complete horusec locally](#requirements-for-use-complete-horusec-locally)
 * [Horusec manager](#horusec-manager)
 * [Contributing](#contributing)
 * [Communication](#communication)
 * [Contributors](#contributors) 
 
 

## What is Horusec?
Horusec is an open source tool that performs static code analysis to identify security flaws during the development process. Currently, the languages for analysis are: C#, Java, Kotlin, Python, Ruby, Golang, Terraform, Javascript, Typescript, Kubernetes, PHP, C, HTML, JSON. The tool has options to search for key leaks and security flaws in all files of your project, as well as in Git history. Horusec can be used by the developer through the CLI and by the DevSecOps team on CI /CD mats. See in our [DOCUMENTATION](https://docs.horusec.io/v/v1-eng/) the complete list of tools and languages that we perform analysis
    
<p align="center" margin="20 0"><img src="assets/horusec-complete-architecture.png" alt="architecture" width="100%" style="max-width:100%;"/></p>

## Project roadmap

We started the project to aggregate within our company, but as the search grew more and more we chose to apply good practices and open it up for everyone to collaborate with this incredible project.

In order to achieve our goals, we separated in some delivery phases:

- **Phase 0:** Analyze vulnerabilities locally and send results to the application to manage them in an analytical way and find points for improvement in the project
- **Phase 1:** SAST analysis of the Kotlin language (Q3)
- **Phase 2:** New visual identity (Q3)
- **Phase 3:** Ability to indicate a vulnerability as a false positive or accepted risk (Q3)
- **Phase 4:** MVP of the SAST analysis engine (Q4 / 2021)
- **Phase 5:** Integration with vulnerability management tools (Archery) (Q4 / 2021)
- **Phase 6:** Plugins in IDE's - Developing in your project and in real time to be able to see if there are any security flaws is very important for the developer. Saving a long time in code review. (Q4 / 2021)

## Getting started

## Installing
To see more details how install go to <a href="horusec-cli#installing">HERE</a>

#### Check the installation
```bash
horusec version
```

## Usage
For use horusec-cli and check your vulnerabilities
```bash
horusec start
```

or send with the authorization token to view the content analytically in the horusec admin panel.

```bash
horusec start -a="<YOUR_TOKEN_AUTHORIZATION>"
```
To acquire the authorization token and you can see your vulnerabilities analytically on our panel see more details <a href="horusec-cli#authorization">HERE</a>


**WARN:** When horusec starts an analysis it creates a folder called `.horusec`. This folder serves as the basis for not changing your code. So we recommend that you add the line `.horusec` into your `.gitignore` file so that this folder does not need to be sent to your git server!

<p align="center" margin="20 0"><img src="assets/usage_horusec.gif" alt="usage_horusec" width="100%" style="max-width:100%;"/></p>

## Requirements for usage horusec-cli
* docker
* git(Mandatory if you are using search throughout the project's git history)

## Usage locally
For usage the horusec locally clone horusec in your local machine and run
```bash
make install
```
and run the [HORUSEC-CLI](horusec-cli#horusec-cli) to start the analysis

### Default Development account
For usage complete feature of the horusec you can see enter using this default user generated by horusec for you usage.

**WARN:** We do dns validation for account creation, so remember to use a valid email. For tests accounts we accept ...@example.com as a valid dns.
```
  email: dev@example.com
  password: Devpass0*
```

### Requirements for use complete horusec locally
* docker
* git
* docker-compose/helm
* golang
* rabbitmq
* postgres
* account-of-email (optional)

## Horusec manager

* Separate repositories by companies
* Manage users who have access to your company (users must be pre-registered on horusec to be invited to a pre-existing company)
* Manage the repositories available in your company for analysis
* Manage users who have access to company repositories
* Manage your access tokens for the specific repository (required to identify which repository this analysis belongs to and save to our system)
* Visually view all existing vulnerabilities in your company and/or its repository

## Contributing

Read our [contributing guide](CONTRIBUTING.md) to learn about our development process, how to propose bugfixes and improvements, and how to build and test your changes to horusec.

## Communication

We have a few channels for contact, feel free to reach out to us at:

- [GitHub Issues](https://github.com/ZupIT/horusec/issues)

## Contributors

This project exists thanks to all the [contributors]((https://github.com/ZupIT/horusec/graphs/contributors)). You rock!   ❤️🚀

[Semgrep]: https://github.com/returntocorp/semgrep
