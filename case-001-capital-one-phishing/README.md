# Case 01: Capital One Phishing Campaign

**Date:** August 9, 2023
**Type:** Credential Harvesting Phishing Attack
**Target Organization:** Capital One (US financial institution)
**Attack Vector:** Malicious HTML attachment
**Status:** Analyzed

## Overview
This is a sophisticated phishing attack impersonating Capital One, a legitimate US financial institution. The attacker registered a fake domain (xserver.com) and hosted it on a Japanese VPS provider (Kagoya) to send fraudulent emails claiming pending payment notifications. The email employs multiple social engineering tactics including urgency ("24-72 hours"), financial incentive ("incoming payment"), and authority mimicry to convince the recipient to download a malicious HTML attachment disguised as a "secure payment verification form." The attachment likely contains a credential-harvesting form designed to steal Capital One login credentials. The email demonstrates advanced phishing techniques by avoiding suspicious links (using an attachment instead) and creating a compelling narrative around a pending payment to increase the likelihood of user interaction.

**See detailed analysis:**
- [Email Analysis](./email-analysis.md)
- [Attachment Analysis](./attachment-analysis.md)
- [Indicators of Compromise](./indicators.md)
- [Findings & Defense Actions](./findings.md)
