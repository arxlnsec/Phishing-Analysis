# Case 03: Perfect Gifts Of 2025 Mass Phishing Campaign

**Date:** October 30, 2025
**Type:** Mass Phishing Campaign
**Attack Vector:** Holiday-themed phishing email with malicious URL
**Target:** Generic (mass mailing to undisclosed recipients)
**Status:** Analyzed (malicious domain now offline)

## Overview
This is a mass phishing campaign leveraging holiday shopping season to distribute malicious content. The attacker impersonates a generic holiday gift retailer called "Perfect Gifts Of 2025" and sends fraudulent emails to large numbers of undisclosed recipients claiming to offer "31 awesome, affordable gifts perfect for xmas this year." Rather than impersonating a specific legitimate brand, the attacker uses a generic branded persona to cast a wider net and increase delivery rates. The email embeds heavily obfuscated malicious URLs within images and text headings that direct users to thempresident.com. The sender uses a domain (wlodmbvsouyasilha.com) with obfuscated naming, combined with Microsoft infrastructure (13.84.221.57) to bypass email filters. Analysis of the malicious URL confirms it was flagged by multiple security vendors as malicious. The campaign appears designed for credential harvesting or phishing scam redirection, targeting users distracted by holiday shopping season who may be less cautious about clicking links. The primary objective is to trick users into clicking the embedded link and either compromising credentials or downloading malicious payloads.

**See detailed analysis:**
- [Email Analysis](./email-analysis.md)
- [URL Analysis](./url-analysis.md)
- [Indicators of Compromise](./indicators.md)
- [Findings & Defense Actions](./findings.md)
