# Case 04: ESaver x Elon Musk Phishing Campaign

**Date:** March 8, 2025
**Type:** Celebrity Impersonation Mass Phishing Campaign
**Attack Vector:** Malicious URLs embedded in image and hyperlinked text
**Target:** Mass mailing to undisclosed recipients
**Status:** Analyzed

## Overview

This is a mass phishing campaign exploiting celebrity impersonation and false authority to distribute malicious content. The attacker falsely claims to be "ESaver x Elon Musk" and advertises a non-existent "ESaver Giveaway" claiming to offer a revolutionary electricity-saving device backed by Elon Musk that provides up to 90% savings on electric bills. The email uses psychological manipulation tactics including congratulations messaging ("You Have Won a ESAVER"), fake urgency ("Don't Miss Out"), false authority (Elon Musk impersonation), and financial incentives ($251 to $15 monthly bill reduction claims) to trick users into clicking malicious links. The sender uses the domain zhishangmingzhan.com with Microsoft infrastructure (135.224.5.224) to bypass email filters. Malicious URLs are embedded within email image and hyperlinked text that direct users to metaverseshades.com, which VirusTotal confirms is malicious with 11/92 vendors flagging phishing and malware. This represents a sophisticated scam targeting individuals seeking financial relief through false technology promises, with the primary objective of credential harvesting or scam redirection.

**See detailed analysis:**

* [Email Analysis](./email-analysis.md)
* [URL Analysis](./url-analysis.md)
* [Indicators of Compromise](./indicators.md)
* [Findings \& Defense Actions](./findings.md)

