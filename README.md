# Ultimate DevSecOps library

## Contribution rules
If you want to contribute to this library of knowledge please create proper PR (Pull Request) with description what you are adding following these set of rules: 

* Clear description of PR (which tool, why, number of stars, maturity and topic) 
* Keep it simple - Fill the description properly
* Fact over feelings or personal opinions
* Add source and follow the library style
* Avoid duplicits - one tool, one topic 
* Try to make bigger updates then on tool link
* Currently open-source only
* Add only active projects 
* Add only security tools 
* Report typos as issue not via PR. 

_Note:_ Currently this is an early version of the library. I recommend PR after first official release. 

**DevSecOps library info:** 

![stars](https://img.shields.io/github/stars/sottlmarek/DevSecOps?style=for-the-badge)
![watchers](https://img.shields.io/github/watchers/sottlmarek/DevSecOps?color=green&style=for-the-badge) ![watchers](https://img.shields.io/github/forks/sottlmarek/DevSecOps?color=orange&style=for-the-badge)

This library contains list of tools and methodologies accompanied with resources. The main goal is to provide to the engineers a guide through opensource DevSecOps tooling. This repository covers only cyber security in the cloud and the DevSecOps scope. 

# Table of Contents

- [Definition](#what-is-devsecops)
- [Tooling](#tooling)
- [Precommit and threat modeling](#pre-commit-time-tools)
- [SAST](#sast)
- [DAST](#dast)
- [Orchestration](#orchestration)
- [Supply chain and dependencies](#oss-and-dependency-management)
- [Infrastructure as code](#infrastructure-as-code-security)
- [Containers security](#containers)
- [Kubernetes](#kubernetes) 
- [Cloud](#multi-cloud)
- [Chaos engineering](#chaos-engineering)
- [Policy as code](#policy-as-code)
- [Methodologies](#methodologies-whitepapers-and-architecture)
- [Other](#other)
- [License](#license) 

# What is DevSecOps 
DevSecOps focuses on security automation, testing and enforcement during DevOps - Release - SDLC cycles. The whole meaning behind this methodology is connecting together Development, Security and Operations. DevSecOps is methodology providing different methods, techniques and processes backed mainly with tooling focusing on developer / security experience. 

DevSecOps takes care that security is part of every stage of DevOps loop - Plan, Code, Build, Test, Release, Deploy, Operate, Monitor. 

Various definitions: 
* https://www.redhat.com/en/topics/devops/what-is-devsecops
* https://www.ibm.com/cloud/learn/devsecops 
* https://snyk.io/series/devsecops/ 
* https://www.synopsys.com/glossary/what-is-devsecops.html
* https://spacelift.io/blog/what-is-devsecops

# Tooling

## Pre-commit time tools

In this section you can find lifecycle helpers, precommit hook tools and threat modeling tools. Threat modeling tools are specific category by themselves allowing you to simulate and discover potential gaps before you start to develop the software or during the process.

Modern DevSecOps tools allow using Threat modeling as code or generation of threat models based on the existing code annotations. 

| Name | URL | Description | Meta | 
| :---------- | :---------- | :---------- | :----------: |
| **git-secrets** | [https://github.com/awslabs/git-secrets](https://github.com/awslabs/git-secrets) | AWS labs tool preventing you from committing secrets to a git repository  |![Git Secrets](https://img.shields.io/github/stars/awslabs/git-secrets?style=for-the-badge) |
| **git-hound** | [https://github.com/tillson/git-hound](https://github.com/tillson/git-hound) | Searchers secrets in git |![git-hound](https://img.shields.io/github/stars/tillson/git-hound?style=for-the-badge) | 
| **goSDL** | [https://github.com/slackhq/goSDL](https://github.com/slackhq/goSDL) |Security Development Lifecycle checklist   |![goSDL](https://img.shields.io/github/stars/slackhq/goSDL?style=for-the-badge) |
| **ThreatPlaybook** | [https://github.com/we45/ThreatPlaybook](https://github.com/we45/ThreatPlaybook) |Threat modeling as code   |![GitLeaks](https://img.shields.io/github/stars/we45/ThreatPlaybook?style=for-the-badge) |
| **Threat Dragon** | [https://github.com/OWASP/threat-dragon](https://github.com/OWASP/threat-dragon) | OWASP Threat modeling tool  |![ThreatDragon](https://img.shields.io/github/stars/OWASP/threat-dragon?style=for-the-badge) |
| **threatspec** | [https://github.com/threatspec/threatspec](https://github.com/threatspec/threatspec) | Threat modeling as code  |![threatspec](https://img.shields.io/github/stars/threatspec/threatspec?style=for-the-badge) |
| **pytm** | [https://github.com/izar/pytm](https://github.com/izar/pytm) | A Pythonic framework for threat modeling  |![pytm](https://img.shields.io/github/stars/izar/pytm?style=for-the-badge) |
| **Threagile** | [https://github.com/Threagile/threagile](https://github.com/Threagile/threagile) | A Go framework for threat modeling  |![Threagile](https://img.shields.io/github/stars/Threagile/threagile?style=for-the-badge) |
| **MAL-lang** | [https://mal-lang.org/#what ](https://mal-lang.org/#what ) | A language to create cyber threat modeling systems for specific domains  |![Mal](https://img.shields.io/github/stars/mal-lang/exampleLang?style=for-the-badge) |
| **Microsoft Threat modeling tool** | [https://docs.microsoft.com/en-us/azure/security/develop/threat-modeling-tool](https://docs.microsoft.com/en-us/azure/security/develop/threat-modeling-tool) | Microsoft threat modeling tool  |![MS Threat modeling tool](https://img.shields.io/github/stars/microsoft/threat-modeling-templates?style=for-the-badge) |
| **Talisman** | [https://github.com/thoughtworks/talisman](https://github.com/thoughtworks/talisman) | A tool to detect and prevent secrets from getting checked in |![Talisman](https://img.shields.io/github/stars/thoughtworks/talisman?style=for-the-badge) |
| **SEDATED** | [https://github.com/OWASP/SEDATED](https://github.com/OWASP/SEDATED) | The SEDATED® Project (Sensitive Enterprise Data Analyzer To Eliminate Disclosure) focuses on preventing sensitive data such as user credentials and tokens from being pushed to Git. |![Talisman](https://img.shields.io/github/stars/OWASP/SEDATED?style=for-the-badge) |
| **Sonarlint** | [https://github.com/SonarSource/sonarlint-core](https://github.com/SonarSource/sonarlint-core) |  Sonar linting utility for IDE |![Sonarlint](https://img.shields.io/github/stars/SonarSource/sonarlint-core?style=for-the-badge)|
| **DevSkim** | [https://github.com/microsoft/DevSkim](https://github.com/microsoft/DevSkim) |  DevSkim is a framework of IDE extensions and language analyzers that provide inline security analysis |![DevSkim](https://img.shields.io/github/stars/microsoft/DevSkim?style=for-the-badge)|
| **detect-secrets** | [https://github.com/Yelp/detect-secrets](https://github.com/Yelp/detect-secrets) |  Detects secrets in your codebase |![DevSkim](https://img.shields.io/github/stars/Yelp/detect-secrets?style=for-the-badge)| 
| **tflint** | [https://github.com/terraform-linters/tflint](https://github.com/terraform-linters/tflint) | A Pluggable Terraform Linter | ![tflint](https://img.shields.io/github/stars/terraform-linters/tflint?style=for-the-badge)|
| **Steampipe Code Plugin** | [https://github.com/turbot/steampipe-plugin-code](https://github.com/turbot/steampipe-plugin-code) | Use SQL to detect secrets from source code and data sources. | [![GitHub stars](https://img.shields.io/github/stars/turbot/steampipe-plugin-code)](https://github.com/turbot/steampipe-plugin-code/stargazers) |

## Secrets management 
Secrets management includes managing, versioning, encryption, discovery, rotating, provisioning of passwords, certificates, configuration values and other types of secrets. 

| Name | URL | Description | Meta | 
| :---------- | :---------- | :---------- | :----------: |
| **GitLeaks** | [https://github.com/zricethezav/gitleaks](https://github.com/zricethezav/gitleaks) | Gitleaks is a scanning tool for detecting hardcoded secrets  |![GitLeaks](https://img.shields.io/github/stars/zricethezav/gitleaks?style=for-the-badge) | 
| **ggshield** | [https://github.com/gitguardian/ggshield](https://github.com/gitguardian/ggshield) | GitGuardian shield (ggshield) is a CLI application that runs in your local environment or in a CI environment and helps you detect more than 350+ types of secrets and sensitive files.  |![ggshield](https://img.shields.io/github/stars/gitguardian/ggshield?style=for-the-badge) |
| **TruffleHog** | [https://github.com/trufflesecurity/truffleHog](https://github.com/trufflesecurity/truffleHog) | TruffleHog is a scanning tool for detecting hardcoded secrets  |![TruffleHog](https://img.shields.io/github/stars/trufflesecurity/truffleHog?style=for-the-badge) |
| **Hashicorp Vault** | [https://github.com/hashicorp/vault](https://github.com/hashicorp/vault) | Hashicorp Vault secrets management  |![Vault](https://img.shields.io/github/stars/hashicorp/vault?style=for-the-badge) |
| **Mozilla SOPS** | [https://github.com/mozilla/sops ](https://github.com/mozilla/sops ) | Mozilla Secrets Operations  |![SOPS](https://img.shields.io/github/stars/mozilla/sops?style=for-the-badge) |
| **AWS secrets manager GH action** | [https://github.com/marketplace/actions/aws-secrets-manager-actions](https://github.com/marketplace/actions/aws-secrets-manager-actions)| AWS secrets manager [docs](https://aws.amazon.com/secrets-manager/) |![AWS Secrets manager action](https://img.shields.io/github/stars/say8425/aws-secrets-manager-actions?style=for-the-badge)|  
| **GitRob** | [https://github.com/michenriksen/gitrob](https://github.com/michenriksen/gitrob) | Gitrob is a tool to help find potentially sensitive files pushed to public repositories on Github  |![GitRob](https://img.shields.io/github/stars/michenriksen/gitrob?style=for-the-badge)|
| **git-wild-hunt** | [https://github.com/d1vious/git-wild-hunt](https://github.com/d1vious/git-wild-hunt ) | A tool to hunt for credentials in the GitHub |![git-wild-hunt](https://img.shields.io/github/stars/d1vious/git-wild-hunt?style=for-the-badge)|
| **aws-vault** | [https://github.com/99designs/aws-vault](https://github.com/99designs/aws-vault) | AWS Vault is a tool to securely store and access AWS credentials in a development environment |![aws-vault](https://img.shields.io/github/stars/99designs/aws-vault?style=for-the-badge)|
| **Knox** | [https://github.com/pinterest/knox](https://github.com/pinterest/knox) | Knox is a service for storing and rotation of secrets, keys, and passwords used by other services |![Knox](https://img.shields.io/github/stars/Pinterest/Knox?style=for-the-badge)|
| **Chef vault** | [https://github.com/chef/chef-vault](https://github.com/chef/chef-vault) |  allows you to encrypt a Chef Data Bag Item |![Chef vault](https://img.shields.io/github/stars/chef/chef-vault?style=for-the-badge)|
| **Ansible vault** | [Ansible vault docs](https://docs.ansible.com/ansible/latest/cli/ansible-vault.html#ansible-vault) |  Encryption/decryption utility for Ansible data files |![Ansible vault](https://img.shields.io/github/stars/ansible-community/ansible-vault?style=for-the-badge)|

## OSS and Dependency management

Dependency security testing and analysis is very important part of discovering supply chain attacks. SBOM creation and following dependency scanning (Software composition analysis) is critical part of continuous integration (CI). Data series and data trends tracking should be part of CI tooling. You need to know what you produce and what you consume in context of libraries and packages. 

| Name | URL | Description | Meta | 
| :---------- | :---------- | :---------- | :----------: |
| **CycloneDX** | [https://github.com/orgs/CycloneDX/repositories](https://github.com/orgs/CycloneDX/repositories) | CycloneDX format for **SBOM** |![CycloneDX](https://img.shields.io/github/stars/CycloneDX/cyclonedx-cli?style=for-the-badge) | 
| **cdxgen** | [https://github.com/AppThreat/cdxgen](https://github.com/AppThreat/cdxgen) | Generates CycloneDX **SBOM**, supports many languages and package managers. |![CycloneDX](https://img.shields.io/github/stars/AppThreat/cdxgen?style=for-the-badge) | 
| **SPDX** | [https://github.com/spdx/spdx-spec](https://github.com/spdx/spdx-spec) | SPDX format for **SBOM** - Software Package Data Exchange |![SpDX](https://img.shields.io/github/stars/spdx/spdx-spec?style=for-the-badge) | 
| **Snyk** | [https://github.com/snyk/snyk](https://github.com/snyk/snyk) | Snyk scans and monitors your projects for security vulnerabilities |![Snyk](https://img.shields.io/github/stars/snyk/snyk?style=for-the-badge) | 
| **vulncost** | [https://github.com/snyk/vulncost](https://github.com/snyk/vulncost) | Security Scanner for VS Code |![Vulncost](https://img.shields.io/github/stars/snyk/vulncost?style=for-the-badge) |
| **Dependency Combobulator** | [https://github.com/apiiro/combobulator](https://github.com/apiiro/combobulator) | Dependency-related attacks detection and prevention through heuristics and insight engine (support multiple dependency schemes) | ![Combobulator](https://img.shields.io/github/stars/apiiro/combobulator?style=for-the-badge) |
| **DependencyTrack** | [https://github.com/DependencyTrack/dependency-track](https://github.com/DependencyTrack/dependency-track) | Dependency security tracking platform |![DependencyTrack](https://img.shields.io/github/stars/DependencyTrack/dependency-track?style=for-the-badge) | 
| **DependencyCheck** | [https://github.com/jeremylong/DependencyCheck](https://github.com/jeremylong/DependencyCheck) | Simple dependency security scanner good for CI |![DependencyCheck](https://img.shields.io/github/stars/jeremylong/DependencyCheck?style=for-the-badge) | 
| **Retire.js** | [https://github.com/retirejs/retire.js/](https://github.com/retirejs/retire.js/) | Helps developers to detect the use of JS-library versions with known vulnerabilities |![Retire.js](https://img.shields.io/github/stars/retirejs/retire.js?style=for-the-badge) |
| **PHP security checker** | [https://github.com/fabpot/local-php-security-checker](https://github.com/fabpot/local-php-security-checker) | Check vulnerabilities in PHP dependencies |![Retire.js](https://img.shields.io/github/stars/fabpot/local-php-security-checker?style=for-the-badge)| 
| **bundler-audit** | [https://github.com/rubysec/bundler-audit](https://github.com/rubysec/bundler-audit) | Patch-level verification for bundler |![Bundler audit](https://img.shields.io/github/stars/rubysec/bundler-audit?style=for-the-badge)| 
| **gemnasium** | [https://gitlab.com/gitlab-org/security-products/analyzers/gemnasium ](https://gitlab.com/gitlab-org/security-products/analyzers/gemnasium ) | Dependency Scanning Analyzer based on Gemnasium || 
| **Dependabot** | [https://github.com/dependabot/dependabot-core](https://github.com/dependabot/dependabot-core) | Automated dependency updates built into GitHub providing security alerts |![Dependabot](https://img.shields.io/github/stars/dependabot/dependabot-core?style=for-the-badge)| 
| **Renovatebot** | [https://github.com/renovatebot/renovate](https://github.com/renovatebot/renovate) | Automated dependency updates, patches multi-platform and multi-language |![Renovatebot](https://img.shields.io/github/stars/renovatebot/renovate?style=for-the-badge)| 
| **npm-check** | [https://www.npmjs.com/package/npm-check](https://www.npmjs.com/package/npm-check) | Check for outdated, incorrect, and unused dependencies. |![npm-check](https://img.shields.io/github/stars/dylang/npm-check?style=for-the-badge)| 
| **Security Scorecards** | [https://securityscorecards.dev](https://securityscorecards.dev) | Checks for several security health metrics on open source libraries and provides a score (0-10) to be considered in the decision making of what libraries to use. |![scorecard](https://img.shields.io/github/stars/ossf/scorecard?style=for-the-badge)| 
| **Syft** | [https://github.com/anchore/syft](https://github.com/anchore/syft) | CLI tool and library for generating an SBOM from container images (and filesystems). |![syft](https://img.shields.io/github/stars/anchore/syft?style=for-the-badge)| 

## Supply chain specific tools 

Supply chain is often the target of attacks. Which libraries you use can have a massive impact on security of the final product (artifacts). CI (continuous integration) must be monitored inside the tasks and jobs in pipeline steps. Integrity checks must be stored out of the system and in ideal case several validation runs with comparison of integrity hashes / or attestation must be performed. 

| Name | URL | Description | Meta | 
| :---------- | :---------- | :---------- | :----------: |
| **Tekton chains** | [https://github.com/tektoncd/chains](https://github.com/tektoncd/chains/) | Kubernetes Custom Resource Definition (CRD) controller that allows you to manage your supply chain security in Tekton. |![Chains](https://img.shields.io/github/stars/tektoncd/chains?style=for-the-badge) | 
| **in-toto** | [https://github.com/in-toto/attestation/tree/v0.1.0/spec](https://github.com/in-toto/attestation/tree/v0.1.0/spec) | An in-toto attestation is authenticated metadata about one or more software artifacts |![in-toto](https://img.shields.io/github/stars/in-toto/attestation?style=for-the-badge) | 
| **SLSA** | [Official GitHub link](https://github.com/slsa-framework/slsa/blob/main/docs/index.md ) | Supply-chain Levels for Software Artifacts |![SLSA](https://img.shields.io/github/stars/slsa-framework/slsa?style=for-the-badge) | 
| **kritis** | [https://github.com/grafeas/kritis](https://github.com/grafeas/kritis) | Solution for securing your software supply chain for Kubernetes apps |![Kritis](https://img.shields.io/github/stars/grafeas/kritis?style=for-the-badge)|
| **ratify** | [https://github.com/deislabs/ratify](https://github.com/deislabs/ratify) | Artifact Ratification Framework |![ratify](https://img.shields.io/github/stars/deislabs/ratify?style=for-the-badge)| 


## SAST

Static code review tools working with source code and looking for known patterns and relationships of methods, variables, classes and libraries. SAST works with the raw code and usually not with build packages. 

| Name | URL | Description | Meta | 
| :---------- | :---------- | :---------- | :----------: |
| **Brakeman** | [https://github.com/presidentbeef/brakeman](https://github.com/presidentbeef/brakeman) | Brakeman is a static analysis tool which checks Ruby on Rails applications for security vulnerabilities|![Brakeman](https://img.shields.io/github/stars/presidentbeef/brakeman?style=for-the-badge) | 
| **Semgrep** | [https://semgrep.dev/](https://semgrep.dev/) | Hi-Quality Open source, works on 17+ languages |![Semgrep](https://img.shields.io/github/stars/returntocorp/semgrep?style=for-the-badge) | 
| **Bandit** | [https://github.com/PyCQA/bandit ](https://github.com/PyCQA/bandit ) | Python specific SAST tool |![Bandit](https://img.shields.io/github/stars/PyCQA/bandit?style=for-the-badge) | 
| **libsast** | [https://github.com/ajinabraham/libsast ](https://github.com/ajinabraham/libsast ) | Generic SAST for Security Engineers. Powered by regex based pattern matcher and semantic aware semgrep |![libsast](https://img.shields.io/github/stars/ajinabraham/libsast?style=for-the-badge) | 
| **ESLint** | [https://eslint.org/](https://eslint.org/) | Find and fix problems in your JavaScript code | | 
| **nodejsscan** | [https://github.com/ajinabraham/nodejsscan](https://github.com/ajinabraham/nodejsscan) | NodeJs SAST scanner with GUI |![NodeJSscan](https://img.shields.io/github/stars/ajinabraham/nodejsscan?style=for-the-badge) | 
| **FindSecurityBugs** | [https://find-sec-bugs.github.io/](https://find-sec-bugs.github.io/) | The SpotBugs plugin for security audits of Java web applications |![FindSecuritybugs](https://img.shields.io/github/stars/find-sec-bugs/find-sec-bugs?style=for-the-badge) | 
| **SonarQube community** | [https://github.com/SonarSource/sonarqube](https://github.com/SonarSource/sonarqube) | Detect security issues in code review with Static Application Security Testing (SAST) |![SonarQube](https://img.shields.io/github/stars/SonarSource/sonarqube?style=for-the-badge) | 
| **gosec** | [https://github.com/securego/gosec](https://github.com/securego/gosec) | Inspects source code for security problems by scanning the Go AST. |![gosec](https://img.shields.io/github/stars/securego/gosec?style=for-the-badge) | 
| **Safety** | [https://github.com/pyupio/safety](https://github.com/pyupio/safety) | Checks Python dependencies for known security vulnerabilities . |![Safety](https://img.shields.io/github/stars/pyupio/safety?style=for-the-badge) | 

**Note:** Semgrep is free CLI tool, however some rulesets (https://semgrep.dev/r) are having various licences, some can be free to use and can be commercial.  

OWASP curated list of SAST tools : https://owasp.org/www-community/Source_Code_Analysis_Tools 

## DAST

Dynamic application security testing (DAST) is a type of application testing (in most cases web) that checks your application from the outside by active communication and analysis of the responses based on injected inputs. DAST tools rely on inputs and outputs to operate. A DAST tool uses these to check for security problems while the software is actually running and is actively deployed on the server (or serverless function).

| Name | URL | Description | Meta | 
| :---------- | :---------- | :---------- | :----------: |
| **Zap proxy** | [https://owasp.org/www-project-zap/](https://owasp.org/www-project-zap/) | Zap proxy providing various docker containers for CI/CD pipeline|![ZAP](https://img.shields.io/github/stars/zaproxy/zaproxy?style=for-the-badge) | 
| **Wapiti** | [https://github.com/wapiti-scanner/wapiti ](https://github.com/wapiti-scanner/wapiti ) | Light pipeline ready scanning tool |![Wapiti](https://img.shields.io/github/stars/wapiti-scanner/wapiti?style=for-the-badge) | 
| **Nuclei** | [https://github.com/projectdiscovery/nuclei](https://github.com/projectdiscovery/nuclei) | Template based security scanning tool |![Nuclei](https://img.shields.io/github/stars/projectdiscovery/nuclei?style=for-the-badge) | 
| **purpleteam** | [https://github.com/purpleteam-labs/purpleteam](https://github.com/purpleteam-labs/purpleteam) | CLI DAST tool incubator project |![purpleteam](https://img.shields.io/github/stars/purpleteam-labs/purpleteam?style=for-the-badge) | 
| **oss-fuzz** | [https://github.com/google/oss-fuzz ](https://github.com/google/oss-fuzz ) | OSS-Fuzz: Continuous Fuzzing for Open Source Software |![osss-fuzz](https://img.shields.io/github/stars/google/oss-fuzz?style=for-the-badge) | 
| **nikto** | [https://github.com/sullo/nikto](https://github.com/sullo/nikto) | Nikto web server scanner |![nikto](https://img.shields.io/github/stars/sullo/nikto?style=for-the-badge) | 
| **skipfish** | [https://code.google.com/archive/p/skipfish/](https://code.google.com/archive/p/skipfish/) | Skipfish is an active web application security reconnaissance tool|![skipfish](https://img.shields.io/github/stars/spinkham/skipfish?style=for-the-badge) | 

## Continuous deployment security

| Name | URL | Description | Meta |
| :---------- | :---------- | :---------- | :----------: |
| **SecureCodeBox** | [https://github.com/secureCodeBox/secureCodeBox](https://github.com/secureCodeBox/secureCodeBox) | Toolchain for continuous scanning of applications and infrastructure |![SCB](https://img.shields.io/github/stars/secureCodeBox/secureCodeBox?style=for-the-badge) | 
| **OpenSCAP** | [https://github.com/OpenSCAP/openscap](https://github.com/OpenSCAP/openscap) | Open Source Security Compliance Solution |![oscap](https://img.shields.io/github/stars/OpenSCAP/openscap?style=for-the-badge) | 
| **ThreatMapper** | [https://github.com/deepfence/ThreatMapper](https://github.com/deepfence/ThreatMapper) | ThreatMapper hunts for vulnerabilities in your production platforms, and ranks these vulnerabilities based on their risk-of-exploit. |![kube-hunter](https://img.shields.io/github/stars/deepfence/ThreatMapper?style=for-the-badge) | 

## Kubernetes 

| Name | URL | Description | Meta | 
| :---------- | :---------- | :---------- | :----------: |
| **KubiScan** | [https://github.com/cyberark/KubiScan](https://github.com/cyberark/KubiScan) | A tool for scanning Kubernetes cluster for risky permissions |![Kubiscan](https://img.shields.io/github/stars/cyberark/kubiscan?style=for-the-badge) | 
| **Kubeaudit** | [https://github.com/Shopify/kubeaudit](https://github.com/Shopify/kubeaudit) | Audit Kubernetes clusters for various different security concerns |![kube-audit](https://img.shields.io/github/stars/Shopify/kubeaudit?style=for-the-badge) | 
| **Kubescape** | [https://github.com/armosec/kubescape](https://github.com/armosec/kubescape) |  The first open-source tool for testing if Kubernetes is deployed according to the NSA-CISA and the MITRE ATT&CK®. |![kubescape](https://img.shields.io/github/stars/armosec/kubescape?style=for-the-badge) |
| **kubesec** | [https://github.com/controlplaneio/kubesec](https://github.com/controlplaneio/kubesec) | Security risk analysis for Kubernetes resources |![kubesec](https://img.shields.io/github/stars/controlplaneio/kubesec?style=for-the-badge) | 
| **kube-bench** | [https://github.com/aquasecurity/kube-bench ](https://github.com/aquasecurity/kube-bench ) | Kubernetes benchmarking tool|![Kubiscan](https://img.shields.io/github/stars/aquasecurity/kube-bench?style=for-the-badge) | 
| **kube-score** | [https://github.com/zegl/kube-score](https://github.com/zegl/kube-score) | Static code analysis of your Kubernetes object definitions |![kube-score](https://img.shields.io/github/stars/zegl/kube-score?style=for-the-badge) | 
| **kube-hunter** | [https://github.com/aquasecurity/kube-hunter](https://github.com/aquasecurity/kube-hunter) | Active scanner for k8s (purple)  |![kube-hunter](https://img.shields.io/github/stars/aquasecurity/kube-hunter?style=for-the-badge) | 
| **Calico** | [https://github.com/projectcalico/calico](https://github.com/projectcalico/calico) | Calico is an open source networking and network security solution for containers  |![Calico](https://img.shields.io/github/stars/projectcalico/calico?style=for-the-badge) | 
| **Krane** | [https://github.com/appvia/krane](https://github.com/appvia/krane) | Simple Kubernetes RBAC static analysis tool |![krane](https://img.shields.io/github/stars/appvia/krane?style=for-the-badge) | 
| **Starboard** | [https://github.com/aquasecurity/starboard](https://github.com/aquasecurity/starboard ) | Starboard inegrates security tools by outputs into Kubernetes CRDs |![starboard](https://img.shields.io/github/stars/aquasecurity/starboard?style=for-the-badge) | 
| **Gatekeeper** | [https://github.com/open-policy-agent/gatekeeper](https://github.com/open-policy-agent/gatekeeper) | Open policy agent gatekeeper for k8s |![gatekeeper](https://img.shields.io/github/stars/open-policy-agent/gatekeeper?style=for-the-badge) | 
| **Inspektor-gadget** | [https://github.com/kinvolk/inspektor-gadget](https://github.com/kinvolk/inspektor-gadget ) | Collection of tools (or gadgets) to debug and inspect k8s |![inspector](https://img.shields.io/github/stars/kinvolk/inspektor-gadget?style=for-the-badge) | 
| **kube-linter** | [https://github.com/stackrox/kube-linter ](https://github.com/stackrox/kube-linter) | Static analysis for Kubernetes |![kube-linter](https://img.shields.io/github/stars/stackrox/kube-linter?style=for-the-badge) | 
| **mizu-api-traffic-viewer** | [https://github.com/up9inc/mizu](https://github.com/up9inc/mizu) | A simple-yet-powerful API traffic viewer for Kubernetes enabling you to view all API communication between microservices to help your debug and troubleshoot regressions. |[![GitHub stars](https://img.shields.io/github/stars/up9inc/mizu)](https://github.com/up9inc/mizu/stargazers) | 
| **HelmSnyk** | [https://github.com/snyk-labs/helm-snyk](https://github.com/snyk-labs/helm-snyk) | The Helm plugin for Snyk provides a subcommand for testing the images. |[![GitHub stars](https://img.shields.io/github/stars/snyk-labs/helm-snyk)](https://github.com/snyk-labs/helm-snyk/stargazers) | 
| **Kubewarden** | [https://github.com/orgs/kubewarden/repositories](https://github.com/orgs/kubewarden/repositories) | Policy as code for kubernetes from SUSE. |[![GitHub stars](https://img.shields.io/github/stars/kubewarden/kwctl)](https://github.com/up9inc/kubewarden/kwctl) | 
| **Kubernetes-sigs BOM** | [https://github.com/kubernetes-sigs/bom](https://img.shields.io/github/stars/kubernetes-sigs/bom) |Kubernetes BOM generator |[![GitHub stars](https://img.shields.io/github/stars/kubernetes-sigs/bom)](https://img.shields.io/github/stars/kubernetes-sigs/bom) | 
| **Capsule** | [https://github.com/clastix/capsule](https://github.com/clastix/capsule) | A multi-tenancy and policy-based framework for Kubernetes |![GitHub stars](https://img.shields.io/github/stars/clastix/capsule) |
| **Badrobot** | [https://github.com/controlplaneio/badrobot](https://github.com/controlplaneio/badrobot) | Badrobot is a Kubernetes Operator audit tool |![GitHub stars](https://img.shields.io/github/stars/controlplaneio/badrobot) |
| **kube-scan** | [https://github.com/octarinesec/kube-scan](https://github.com/octarinesec/kube-scan) |  k8s cluster risk assessment tool | ![kube-scan](https://img.shields.io/github/stars/octarinesec/kube-scan?style=for-the-badge)
| **Istio** | [https://istio.io](https://istio.io) | Istio is a service mesh based on Envoy. Engage encryption, role-based access, and authentication across services. |![GitHub stars](https://img.shields.io/github/stars/istio/istio) |
| **Kubernetes Insights** | [https://github.com/turbot/steampipe-mod-kubernetes-insights](https://github.com/turbot/steampipe-mod-kubernetes-insights) | Visualize Kubernetes inventory and permissions through relationship graphs. | [![GitHub stars](https://img.shields.io/github/stars/turbot/steampipe-mod-kubernetes-insights)](https://github.com/turbot/steampipe-mod-kubernetes-insights/stargazers) |
| **Kubernetes Compliance** | [https://github.com/turbot/steampipe-mod-kubernetes-compliance](https://github.com/turbot/steampipe-mod-kubernetes-compliance) | Check compliance of Kubernetes configurations to security best practices. | [![GitHub stars](https://img.shields.io/github/stars/turbot/steampipe-mod-kubernetes-compliance)](https://github.com/turbot/steampipe-mod-kubernetes-compliance/stargazers) |

## Containers 

| Name | URL | Description | Meta | 
| :---------- | :---------- | :---------- | :----------: |
| **Harbor** | [https://github.com/goharbor/harbor](https://github.com/goharbor/harbor) | Trusted cloud native registry project|![Harbor](https://img.shields.io/github/stars/goharbor/harbor?style=for-the-badge) | 
| **Anchore** | [https://github.com/anchore/anchore-engine](https://github.com/anchore/anchore-engine) | Centralized service for inspection, analysis, and certification of container images |![Anchore](https://img.shields.io/github/stars/anchore/anchore-engine?style=for-the-badge) | 
| **Clair** | [https://github.com/quay/clair](https://github.com/quay/clair) | Docker vulnerability scanner|![Clair](https://img.shields.io/github/stars/goharbor/harbor?style=for-the-badge) | 
| **Deepfence ThreatMapper** | [https://github.com/deepfence/ThreatMapper](https://github.com/deepfence/ThreatMapper) | Apache v2, powerful runtime vulnerability scanner for kubernetes, virtual machines and serverless. | ![ThreatMapper](https://img.shields.io/github/stars/deepfence/ThreatMapper?style=for-the-badge) | 
| **Docker bench** | [https://github.com/docker/docker-bench-security ](https://github.com/docker/docker-bench-security ) | Docker benchmarking against CIS|![docker bench](https://img.shields.io/github/stars/goharbor/harbor?style=for-the-badge)| 
| **Falco** | [https://github.com/falcosecurity/falco](https://github.com/falcosecurity/falco) | Container runtime protection |![Falco](https://img.shields.io/github/stars/falcosecurity/falco?style=for-the-badge) | 
| **Trivy** | [https://github.com/aquasecurity/trivy](https://github.com/aquasecurity/trivy) | Comprehensive scanner for vulnerabilities in container images |![Trivy](https://img.shields.io/github/stars/aquasecurity/trivy?style=for-the-badge) | 
| **Notary** | [https://github.com/notaryproject/notary](https://github.com/notaryproject/notary) | Docker signing|![Notary](https://img.shields.io/github/stars/notaryproject/notary?style=for-the-badge) | 
| **Cosign** | [https://github.com/sigstore/cosign](https://github.com/sigstore/cosign) | Container signing|![Cosign](https://img.shields.io/github/stars/sigstore/cosign?style=for-the-badge) | 
| **watchtower** | [https://github.com/containrrr/watchtower](https://github.com/containrrr/watchtower) | Updates the running version of your containerized app |![watchtower](https://img.shields.io/github/stars/containrrr/watchtower?style=for-the-badge) |
| **Grype** | [https://github.com/anchore/grype](https://github.com/anchore/grype) | Vulnerability scanner for container images (and also filesystems). |![Grype](https://img.shields.io/github/stars/anchore/grype?style=for-the-badge) |

## Multi-Cloud 

| Name | URL | Description | Meta | 
| :---------- | :---------- | :---------- | :----------: |
| **Cloudsploit** | [https://github.com/aquasecurity/cloudsploit](https://github.com/aquasecurity/cloudsploit) | Detection of security risks in cloud infrastructure |![Cloudsploit](https://img.shields.io/github/stars/aquasecurity/cloudsploit?style=for-the-badge) |
| **ScoutSuite** | [https://github.com/nccgroup/ScoutSuite](https://github.com/nccgroup/ScoutSuite) | NCCgroup mutlicloud scanning tool |![ScoutSuite](https://img.shields.io/github/stars/nccgroup/ScoutSuite?style=for-the-badge) |
| **CloudCustodian** | [https://github.com/cloud-custodian/cloud-custodian/](https://github.com/cloud-custodian/cloud-custodian/) | Multicloud security analysis framework |![CloudCustodian](https://img.shields.io/github/stars/cloud-custodian/cloud-custodian?style=for-the-badge) | 
| **CloudGraph** | [https://github.com/cloudgraphdev/cli](https://github.com/cloudgraphdev/cli) | GraphQL API + Security for AWS, Azure, GCP, and K8s |![CloudGraph](https://img.shields.io/github/stars/cloudgraphdev/cli?style=for-the-badge) |
| **Steampipe** | [https://github.com/turbot/steampipe](https://github.com/turbot/steampipe) | Instantly query your cloud, code, logs & more with SQL. Build on thousands of open-source benchmarks & dashboards for security & insights. | [![GitHub stars](https://img.shields.io/github/stars/turbot/steampipe)](https://github.com/turbot/steampipe/stargazers) |

## AWS 

AWS specific DevSecOps tooling. Tools here cover different areas like inventory management, misconfiguration scanning or IAM roles and policies review. 

| Name | URL | Description | Meta | 
| :---------- | :---------- | :---------- | :----------: |
| **Dragoneye** | [https://github.com/indeni/dragoneye](https://github.com/indeni/dragoneye) | Dragoneye Indeni AWS scanner |![Dragoneye](https://img.shields.io/github/stars/indeni/dragoneye?style=for-the-badge) |
| **Prowler** | [https://github.com/toniblyx/prowler](https://github.com/toniblyx/prowler) | Prowler is a command line tool that helps with AWS security assessment, auditing, hardening and incident response. |![Prowler](https://img.shields.io/github/stars/toniblyx/prowler?style=for-the-badge) |
| **aws-inventory** | [https://github.com/nccgroup/aws-inventory](https://github.com/nccgroup/aws-inventory) | Helps to discover all AWS resources created in an account|![aws-inventory](https://img.shields.io/github/stars/nccgroup/aws-inventory?style=for-the-badge) |
| **PacBot** | [https://github.com/tmobile/pacbot](https://github.com/tmobile/pacbot) | Policy as Code Bot (PacBot)|![pacbot](https://img.shields.io/github/stars/tmobile/pacbot?style=for-the-badge) |
| **Komiser** | [https://github.com/mlabouardy/komiser](https://github.com/mlabouardy/komiser) | Monitoring dashboard for costs and security|![komiser](https://img.shields.io/github/stars/mlabouardy/komiser?style=for-the-badge) |
| **Cloudsplaining** | [https://github.com/salesforce/cloudsplaining](https://github.com/salesforce/cloudsplaining) | IAM analysis framework |![cloudsplaining](https://img.shields.io/github/stars/salesforce/cloudsplaining?style=for-the-badge) |
| **ElectricEye** | [https://github.com/jonrau1/ElectricEye](https://github.com/jonrau1/ElectricEye) | Continuously monitor your AWS services for configurations |![ElectricEye](https://img.shields.io/github/stars/jonrau1/ElectricEye?style=for-the-badge) |
| **Cloudmapper** | [https://github.com/duo-labs/cloudmapper](https://github.com/duo-labs/cloudmapper ) | CloudMapper helps you analyze your Amazon Web Services (AWS) environments |![cloudmapper](https://img.shields.io/github/stars/duo-labs/cloudmapper?style=for-the-badge) | 
| **cartography** | [https://github.com/lyft/cartography](https://github.com/lyft/cartography) | Consolidates AWS infrastructure assets and the relationships between them in an intuitive graph |![cartography](https://img.shields.io/github/stars/lyft/cartography?style=for-the-badge) | 
| **policy_sentry** | [https://github.com/salesforce/policy_sentry](https://github.com/salesforce/policy_sentry ) | IAM Least Privilege Policy Generator |![policycentry](https://img.shields.io/github/stars/salesforce/policy_sentry?style=for-the-badge) | 
| **AirIAM** | [https://github.com/bridgecrewio/AirIAM](https://github.com/bridgecrewio/AirIAM) | IAM Least Privilege anmalyzer and Terraformer |![AirIam](https://img.shields.io/github/stars/bridgecrewio/AirIAM?style=for-the-badge) | 
| **StreamAlert** | [https://github.com/airbnb/streamalert](https://github.com/airbnb/streamalert ) | AirBnB serverless, real-time data analysis framework which empowers you to ingest, analyze, and alert  |![StreamAlert](https://img.shields.io/github/stars/airbnb/streamalert?style=for-the-badge) | 
| **CloudQuery** | [https://github.com/cloudquery/cloudquery/](https://github.com/cloudquery/cloudquery/) | AirBnB serverless, real-time data analysis framework which empowers you to ingest, analyze, and alert  |![CloudQuery](https://img.shields.io/github/stars/cloudquery/cloudquery?style=for-the-badge) | 
| **S3Scanner** | [https://github.com/sa7mon/S3Scanner/](https://github.com/cloudquery/cloudquery/) | A tool to find open S3 buckets and dump their contents  |![S3Scanner](https://img.shields.io/github/stars/sa7mon/S3Scanner?style=for-the-badge) | 
| **aws-iam-authenticator** | [https://github.com/kubernetes-sigs/aws-iam-authenticator/](https://github.com/kubernetes-sigs/aws-iam-authenticator/) | A tool to use AWS IAM credentials to authenticate to a Kubernetes cluster |![authenticator](https://img.shields.io/github/stars/kubernetes-sigs/aws-iam-authenticator?style=for-the-badge) | 
| **kube2iam** | [https://github.com/jtblin/kube2iam/](https://github.com/jtblin/kube2iam/) | A tool to use AWS IAM credentials to authenticate to a Kubernetes cluster |![kube2iam](https://img.shields.io/github/stars/jtblin/kube2iam?style=for-the-badge) | 
| **AWS open source security samples** | [Official AWS opensource repo](https://github.com/orgs/aws-samples/repositories?language=&q=security&sort=&type=) |Collection of official AWS open-source resources | ![Amazon AWS](https://img.shields.io/static/v1?style=for-the-badge&message=Amazon+AWS&color=232F3E&logo=Amazon+AWS&logoColor=FFFFFF&label=)| 
| **AWS Firewall factory** | [Globaldatanet FMS automation](https://github.com/globaldatanet/aws-firewall-factory) |Deploy, update, and stage your WAFs while managing them centrally via FMS | ![Globaldatanet Firewall factory](https://img.shields.io/github/stars/globaldatanet/aws-firewall-factory?style=for-the-badge)| 
| **Parliment** | [Parliment](https://github.com/duo-labs/parliament) | Parliament is an AWS IAM linting library | ![IAM linting](https://img.shields.io/github/stars/duo-labs/parliament?style=for-the-badge)| 
| **Yor** | [Yor](https://github.com/bridgecrewio/yor) | Adds informative and consistent tags across infrastructure-as-code frameworks such as Terraform, CloudFormation, and Serverless | ![Yor](https://img.shields.io/github/stars/bridgecrewio/yor?style=for-the-badge)|
| **AWS Insights** | [https://github.com/turbot/steampipe-mod-aws-insights](https://github.com/turbot/steampipe-mod-aws-insights) | Visualize AWS inventory and permissions through relationship graphs. | [![GitHub stars](https://img.shields.io/github/stars/turbot/steampipe-mod-aws-insights)](https://github.com/turbot/steampipe-mod-aws-insights/stargazers) |
| **AWS Compliance** | [https://github.com/turbot/steampipe-mod-aws-compliance](https://github.com/turbot/steampipe-mod-aws-compliance) | Check compliance of AWS configurations to security best practices. | [![GitHub stars](https://img.shields.io/github/stars/turbot/steampipe-mod-aws-compliance)](https://github.com/turbot/steampipe-mod-aws-compliance/stargazers) |


## Google cloud platform 

GCP specific DevSecOps tooling. Tools here cover different areas like inventory management, misconfiguration scanning or IAM roles and policies review. 

| Name | URL | Description | Meta | 
| :---------- | :---------- | :---------- | :----------: |
| **Forseti** | [https://github.com/forseti-security/forseti-security](https://github.com/forseti-security/forseti-security) | Complex security orchestration and scanning platform | ![Forseti](https://img.shields.io/github/stars/forseti-security/forseti-security?style=for-the-badge)|
| **GCP Insights** | [https://github.com/turbot/steampipe-mod-gcp-insights](https://github.com/turbot/steampipe-mod-gcp-insights) | Visualize GCP inventory and permissions through relationship graphs. | [![GitHub stars](https://img.shields.io/github/stars/turbot/steampipe-mod-gcp-insights)](https://github.com/turbot/steampipe-mod-gcp-insights/stargazers) |
| **GCP Compliance** | [https://github.com/turbot/steampipe-mod-gcp-compliance](https://github.com/turbot/steampipe-mod-gcp-compliance) | Check compliance of GCP configurations to security best practices. | [![GitHub stars](https://img.shields.io/github/stars/turbot/steampipe-mod-gcp-compliance)](https://github.com/turbot/steampipe-mod-gcp-compliance/stargazers) |


## Microsoft Azure 

Azure specific DevSecOps tooling. Tools here cover different areas like inventory management, misconfiguration scanning or IAM roles and policies review. 

| Name | URL | Description | Meta | 
| :---------- | :---------- | :---------- | :----------: |
| **Azure Insights** | [https://github.com/turbot/steampipe-mod-azure-insights](https://github.com/turbot/steampipe-mod-azure-insights) | Visualize Azure inventory and permissions through relationship graphs. | [![GitHub stars](https://img.shields.io/github/stars/turbot/steampipe-mod-azure-insights)](https://github.com/turbot/steampipe-mod-azure-insights/stargazers) |
| **Azure Compliance** | [https://github.com/turbot/steampipe-mod-azure-compliance](https://github.com/turbot/steampipe-mod-azure-compliance) | Check compliance of Azure configurations to security best practices. | [![GitHub stars](https://img.shields.io/github/stars/turbot/steampipe-mod-azure-compliance)](https://github.com/turbot/steampipe-mod-azure-compliance/stargazers) |

## Policy as code

Policy as code is the idea of writing code in a high-level language to manage and automate policies. By representing policies as code in text files, proven software development best practices can be adopted such as version control, automated testing, and automated deployment. (Source: https://docs.hashicorp.com/sentinel/concepts/policy-as-code)

| Name | URL | Description | Meta | 
| :---------- | :---------- | :---------- | :----------: |
| **Open Policy agent** | [https://github.com/open-policy-agent/opa](https://github.com/open-policy-agent/opa) | General-purpose policy engine that enables unified, context-aware policy enforcement across the entire stack |![OPA](https://img.shields.io/github/stars/open-policy-agent/opa?style=for-the-badge) |
| **Kyverno** | [https://github.com/kyverno/kyverno](https://github.com/kyverno/kyverno) | Kyverno is a policy engine designed for Kubernetes |![kyverno](https://img.shields.io/github/stars/kyverno/kyverno?style=for-the-badge) | 
| **Inspec** | [https://github.com/inspec/inspec](https://github.com/inspec/inspec) | Chef InSpec is an open-source testing framework for infrastructure with a human- and machine-readable language for specifying compliance, security and policy requirements. |![Inspec](https://img.shields.io/github/stars/inspec/inspec?style=for-the-badge) | 
| **Cloud Formation guard** | [https://github.com/aws-cloudformation/cloudformation-guard](https://github.com/aws-cloudformation/cloudformation-guard) | Cloud Formation policy as code |![cf-guard](https://img.shields.io/github/stars/aws-cloudformation/cloudformation-guard?style=for-the-badge) |
| **cnspec** | [https://github.com/mondoohq/cnspec](https://github.com/mondoohq/cnspec) | cnspec is a cloud-native and powerful Policy as Code engine to assess the security and compliance of your business-critical infrastructure. cnspec finds vulnerabilities and misconfigurations on all systems in your infrastructure including: public and private cloud environments, Kubernetes clusters, containers, container registries, servers and endpoints, SaaS products, infrastructure as code, APIs, and more. |![cf-guard](https://img.shields.io/github/stars/mondoohq/cnspec?style=for-the-badge) |


## Chaos engineering

Chaos Engineering is the discipline of experimenting on a system in order to build confidence in the system’s capability to withstand turbulent conditions in production.

Reading and manifestos: https://principlesofchaos.org/

| Name | URL | Description | Meta | 
| :---------- | :---------- | :---------- | :----------: |
| **chaos-mesh** | [https://github.com/chaos-mesh/chaos-mesh](https://github.com/chaos-mesh/chaos-mesh) | It is a cloud-native Chaos Engineering platform that orchestrates chaos on Kubernetes environments |![Chaos mesh](https://img.shields.io/github/stars/chaos-mesh/chaos-mesh?style=for-the-badge) |
| **Chaos monkey** | [https://netflix.github.io/chaosmonkey/](https://netflix.github.io/chaosmonkey/) | Chaos Monkey is responsible for randomly terminating instances in production to ensure that engineers implement their services to be resilient to instance failures. |![Chaos monkey](https://img.shields.io/github/stars/Netflix/chaosmonkey?style=for-the-badge) |
| **Chaos Engine** | [https://thalesgroup.github.io/chaos-engine/](https://thalesgroup.github.io/chaos-engine/) | The Chaos Engine is a tool that is designed to intermittently destroy or degrade application resources running in cloud based infrastructure. These events are designed to occur while the appropriate resources are available to resolve the issue if the platform fails to do so on it's own. |![Chaos Engine](https://img.shields.io/github/stars/thalesgroup/chaos-engine?style=for-the-badge) |
| **chaoskube** | [https://github.com/linki/chaoskube ](https://github.com/linki/chaoskube ) | Test how your system behaves under arbitrary pod failures. |![chaoskube](https://img.shields.io/github/stars/linki/chaoskube?style=for-the-badge) |
| **Kube-Invaders** | [https://github.com/lucky-sideburn/KubeInvaders](https://github.com/lucky-sideburn/KubeInvaders) | Gamified chaos engineering tool for Kubernetes |![chaoskube](https://img.shields.io/github/stars/lucky-sideburn/KubeInvaders?style=for-the-badge) |
| **kube-monkey** | [https://github.com/asobti/kube-monkey](https://github.com/asobti/kube-monkey) | Gamified chaos engineering tool for Kubernetes |![kube-monkey](https://img.shields.io/github/stars/asobti/kube-monkey?style=for-the-badge) |
| **Litmus Chaos** | [https://litmuschaos.io/](https://litmuschaos.io/) | Litmus is an end-to-end chaos engineering platform for cloud native infrastructure and applications. Litmus is designed to orchestrate and analyze chaos in their environments. | ![Litmus](https://img.shields.io/github/stars/litmuschaos/litmus?style=for-the-badge) |
| **Gremlin** | [https://github.com/gremlin/gremlin-python](https://github.com/gremlin/gremlin-python) | Chaos enginnering SaaS platform with free plan and some open source libraries |![Gremlin](https://img.shields.io/github/stars/gremlin/gremlin-python?style=for-the-badge) |
| **AWS FIS samples** | [https://github.com/aws-samples/aws-fault-injection-simulator-samples](https://github.com/aws-samples/aws-fault-injection-simulator-samples) | AWS Fault injection simulator samples |![AWS](https://img.shields.io/github/stars/aws-samples/aws-fault-injection-simulator-samples?style=for-the-badge) |
| **CloudNuke** | [https://github.com/gruntwork-io/cloud-nuke](https://github.com/gruntwork-io/cloud-nuke) | CLI tool to delete all resources in an AWS account |![CloudNuke](https://img.shields.io/github/stars/gruntwork-io/cloud-nuke?style=for-the-badge) |

## Infrastructure as code security 

Scanning your infrastructure when it is only code helps shift-left the security. Many tools offer in IDE scanning and providing real-time advisory do Cloud engineers. 

| Name | URL | Description | Meta |
| :---------- | :---------- | :---------- | :----------: |
| **KICS** | [https://github.com/Checkmarx/kics](https://github.com/Checkmarx/kics) | Checkmarx security testing opensource for IaC |![Checkmarx](https://img.shields.io/github/stars/Checkmarx/kics?style=for-the-badge) | 
| **Checkov** | [https://github.com/bridgecrewio/checkov](https://github.com/bridgecrewio/checkov) | Checkov is a static code analysis tool for infrastructure-as-code |![Checkov](https://img.shields.io/github/stars/bridgecrewio/checkov?style=for-the-badge) | 
| **tfsec** | [https://github.com/aquasecurity/tfsec](https://github.com/aquasecurity/tfsec) | tfsec uses static analysis of your terraform templates to spot potential security issues. Now with terraform CDK support |![tfsec](https://img.shields.io/github/stars/aquasecurity/tfsec?style=for-the-badge) | 
| **terrascan** | [https://github.com/accurics/terrascan](https://github.com/accurics/terrascan) | Terrascan is a static code analyzer for Infrastructure as Code |![terrascan](https://img.shields.io/github/stars/accurics/terrascan?style=for-the-badge) | 
| **cfsec** | [https://github.com/aquasecurity/cfsec](https://github.com/aquasecurity/cfsec) | cfsec scans CloudFormation configuration files for security issues |![cfsec](https://img.shields.io/github/stars/aquasecurity/cfsec?style=for-the-badge) | 
| **cfn_nag** | [https://github.com/stelligent/cfn_nag](https://github.com/stelligent/cfn_nag) |  Looks for insecure patterns in CloudFormation |![cfnag](https://img.shields.io/github/stars/stelligent/cfn_nag?style=for-the-badge) | 
| **Sysdig IaC scanner action** | [https://github.com/sysdiglabs/cloud-iac-scanner-action](https://github.com/sysdiglabs/cloud-iac-scanner-action) |  Scans your repository with Sysdig IAC Scanner and report the vulnerabilities. |![sysdig iac scanner](https://img.shields.io/github/stars/sysdiglabs/cloud-iac-scanner-action?style=for-the-badge) |
| **Terraform Compliance for AWS** | [https://github.com/turbot/steampipe-mod-terraform-aws-compliance](https://github.com/turbot/steampipe-mod-terraform-aws-compliance) | Check compliance of Terraform configurations to AWS security best practices. | [![GitHub stars](https://img.shields.io/github/stars/turbot/steampipe-mod-terraform-aws-compliance)](https://github.com/turbot/steampipe-mod-terraform-aws-compliance/stargazers) |
| **Terraform Compliance for Azure** | [https://github.com/turbot/steampipe-mod-terraform-azure-compliance](https://github.com/turbot/steampipe-mod-terraform-azure-compliance) | Check compliance of Terraform configurations to Azure security best practices. | [![GitHub stars](https://img.shields.io/github/stars/turbot/steampipe-mod-terraform-azure-compliance)](https://github.com/turbot/steampipe-mod-terraform-azure-compliance/stargazers) |
| **Terraform Compliance for GCP** | [https://github.com/turbot/steampipe-mod-terraform-gcp-compliance](https://github.com/turbot/steampipe-mod-terraform-gcp-compliance) | Check compliance of Terraform configurations to GCP security best practices. | [![GitHub stars](https://img.shields.io/github/stars/turbot/steampipe-mod-terraform-gcp-compliance)](https://github.com/turbot/steampipe-mod-terraform-gcp-compliance/stargazers) |
| **Terraform Compliance for OCI** | [https://github.com/turbot/steampipe-mod-terraform-oci-compliance](https://github.com/turbot/steampipe-mod-terraform-oci-compliance) | Check compliance of Terraform configurations to OCI security best practices. | [![GitHub stars](https://img.shields.io/github/stars/turbot/steampipe-mod-terraform-oci-compliance)](https://github.com/turbot/steampipe-mod-terraform-oci-compliance/stargazers) |

## Orchestration 

Event driven security help to drive, automate and execute tasks for security processes. The tools here and not dedicated security tools but are helping to automate and orchestrate security tasks or are part of most modern security automation frameworks or tools. 

| Name | URL | Description | Meta |
| :---------- | :---------- | :---------- | :----------: |
| **StackStorm** | [https://github.com/StackStorm/st2](https://github.com/StackStorm/st2) | Platform for integration and automation across services and tools supporting event driven security |![StackStorm](https://img.shields.io/github/stars/StackStorm/st2?style=for-the-badge) | 
| **Camunda** | [https://github.com/camunda/camunda-bpm-platform](https://github.com/camunda/camunda-bpm-platform) | Workflow and process automation |![Camunda](https://img.shields.io/github/stars/camunda/camunda-bpm-platform?style=for-the-badge)| 
| **DefectDojo** | [https://github.com/DefectDojo/django-DefectDojo](https://github.com/DefectDojo/django-DefectDojo) | Security orchestration and vulnerability management platform |![DefectDojo](https://img.shields.io/github/stars/DefectDojo/django-DefectDojo?style=for-the-badge) | 
| **Faraday** | [https://github.com/infobyte/faraday](https://github.com/infobyte/faraday) | Security suite for Security Orchestration, vulnerability management and centralized information |![Faraday](https://img.shields.io/github/stars/infobyte/faraday) |

# Methodologies, whitepapers and architecture

List of resources worth investigating: 
* https://dodcio.defense.gov/Portals/0/Documents/DoD%20Enterprise%20DevSecOps%20Reference%20Design%20v1.0_Public%20Release.pdf
* https://dodcio.defense.gov/Portals/0/Documents/Library/DoDEnterpriseDevSecOpsStrategyGuide.pdf 
* https://csrc.nist.gov/publications/detail/sp/800-204c/draft 
* https://owasp.org/www-project-devsecops-maturity-model/ 
* https://www.sans.org/posters/cloud-security-devsecops-best-practices/ 

AWS DevOps whitepapers: 
* https://d1.awsstatic.com/whitepapers/aws-development-test-environments.pdf
* https://d1.awsstatic.com/whitepapers/AWS_DevOps.pdf
* https://d1.awsstatic.com/whitepapers/AWS_Blue_Green_Deployments.pdf
* https://d1.awsstatic.com/whitepapers/DevOps/import-windows-server-to-amazon-ec2.pdf
* https://d1.awsstatic.com/whitepapers/DevOps/Jenkins_on_AWS.pdf
* https://d1.awsstatic.com/whitepapers/DevOps/practicing-continuous-integration-continuous-delivery-on-AWS.pdf
* https://d1.awsstatic.com/whitepapers/DevOps/infrastructure-as-code.pdf
* https://d1.awsstatic.com/whitepapers/microservices-on-aws.pdf
* https://d1.awsstatic.com/whitepapers/DevOps/running-containerized-microservices-on-aws.pdf 
* https://d1.awsstatic.com/Marketplace/solutions-center/downloads/AppSec-DevSecOps-AWS-SANS-eBook.pdf (AWS + SANS whitepaper)

AWS blog: 
* https://aws.amazon.com/blogs/devops/building-end-to-end-aws-devsecops-ci-cd-pipeline-with-open-source-sca-sast-and-dast-tools/
* https://aws.amazon.com/blogs/devops/building-an-end-to-end-kubernetes-based-devsecops-software-factory-on-aws/ 

Microsoft whitepapers: 
* https://azure.microsoft.com/mediahandler/files/resourcefiles/6-tips-to-integrate-security-into-your-devops-practices/DevSecOps_Report_Tips_D6_fm.pdf 
* https://docs.microsoft.com/en-us/azure/architecture/solution-ideas/articles/devsecops-in-azure 
* https://docs.microsoft.com/en-us/azure/architecture/solution-ideas/articles/devsecops-in-github 

GCP whitepapers: 
* https://cloud.google.com/architecture/devops/devops-tech-shifting-left-on-security 
* https://cloud.google.com/security/overview/whitepaper 
* https://services.google.com/fh/files/misc/security_whitepapers_march2018.pdf 
* https://cloud.google.com/security/encryption-in-transit/application-layer-transport-security 
* https://services.google.com/fh/files/misc/google-cloud-security-foundations-guide.pdf

# Other

Here are the other links and resources that do not fit in any previous category. They can meet multiple categories in time or help you in your learning. 

| Name | URL | Description | Meta | 
| :---------- | :---------- | :---------- | :----------: |
| **Automated Security Helper (ASH)** | [https://github.com/aws-samples/automated-security-helper](https://github.com/aws-samples/automated-security-helper) | ASH is a one stop shop for security scanners, and does not require any installation. It will identify the different frameworks, and download the relevant, up to date tools. ASH is running on isolated Docker containers, keeping the user environment clean, with a single aggregated report. The following frameworks are supported: Git, Python, Javascript, Cloudformation, Terraform and Jupyter Notebooks.  |![ASH](https://img.shields.io/github/stars/aws-samples/automated-security-helper?style=for-the-badge) | 
| **Mobile security framework** | [https://github.com/MobSF/Mobile-Security-Framework-MobSF](https://github.com/MobSF/Mobile-Security-Framework-MobSF) | SAST, DAST and pentesting tool for mobile apps |![MobSF](https://img.shields.io/github/stars/MobSF/Mobile-Security-Framework-MobSF?style=for-the-badge) |
| **Legitify** | [https://github.com/Legit-Labs/legitify](https://github.com/Legit-Labs/legitify) | Detect and remediate misconfigurations and security risks across all your GitHub and GitLab assets  |![Legitify](https://img.shields.io/github/stars/Legit-Labs/legitify?style=for-the-badge) |

Training - https://www.practical-devsecops.com/devsecops-university/ 

DevSecOps videos - [Hackitect playground](https://www.youtube.com/channel/UCy0S_HftNM7Fy0ksEOUHc-Q)

# License
MIT license

Marek Šottl (c) 2022
