# Administrative Template (ADMX) for Microsoft Defender Attack Surface Reduction (ASR)

## Introduction

Attack surface reduction rules (ASR) are optional features of Microsoft Defender Antivirus. These rules target certain software behaviors, such as:

- Launching executable files and scripts that attempt to download or run files.
- Running obfuscated or otherwise suspicious scripts.
- Performing behaviors that apps don't usually initiate during normal day-to-day work.

Such software behaviors are sometimes seen in legitimate applications. However, these behaviors are often considered risky because they're commonly abused by attackers through malware. Attack surface reduction rules can constrain software-based risky behaviors and help keep your organization safe.

ASR deployment through Active Directory Group Policies (GPO) can be tricky, as it requires the knowledge of rule identifiers:

![ASR configuration using the Microsoft-provided GPO template](/images/builtin-admx-editor.png)

The aim of this project is to greatly improve the user experience by providing a custom administrative template with a standalone setting for each ASR rule:

![List of custom settings in the GPO editor](/images/custom-admx-settings-list.png)

![Custom ASR rule editor](/images/policy-editor.png)

![Group Policy Result](/images/group-policy-result.png)

## Installation

Just copy the ADMX and ADML files into the [local or central ADMX store](https://msdn.microsoft.com/en-us/library/bb530196.aspx#manageadmxfiles_topic2).

## Known Issues

Due to the technical limitations of the Group Policy Editor,
the policies can only be set to **Enabled** or **Not Configured**.

## References

The ADMX template is based on the following official documents:

- [Attack surface reduction rules reference](https://learn.microsoft.com/en-us/defender-endpoint/attack-surface-reduction-rules-reference)
- [Enable attack surface reduction rules](https://learn.microsoft.com/en-us/defender-endpoint/enable-attack-surface-reduction#group-policy)
