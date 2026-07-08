# Case 02: ELLIPAL Wallet Phishing Campaign

**Date:** April 16, 2026
**Type:** Credential Harvesting Phishing Attack
**Target Organization:** ELLIPAL Wallet (Cryptocurrency Hardware Wallet)
**Attack Vector:** Domain typosquatting + malicious URL
**Status:** Analyzed

## Overview
This email is a sophisticated phishing attack impersonating ELLIPAL Wallet, a legitimate cold storage cryptocurrency hardware wallet. The attacker falsely claims to introduce a new "ELLIPAL Desktop Wallet" application, which does not officially exist. ELLIPAL only manufactures hardware wallets and has no legitimate desktop software. The sender uses BIGLOBE email service (xa6yw6@bma.biglobe.ne.jp), a Japanese Internet Service Provider owned by KDDI Corporation. Since the attacker is using a legitimate email service, authentication result shows spf, dkim and dmarc as pass but KDDI Corporation or BIGLOBE has no legitimate connection with Ellipal Wallet. Users are directed to a fake domain (ellipalwallet.io) that closely mimics the legitimate ELLIPAL domain (ellipal.com). The primary objective is credential harvesting, tricking users into downloading malicious software or divulging sensitive information such as seed phrases or private cryptocurrency keys. This represents a high-risk attack targeting cryptocurrency users who may be less cautious about downloading wallet management software. 

**See detailed analysis:**
- [Email Analysis](./email-analysis.md)
- [URL Analysis](./url-analysis.md)
- [Indicators of Compromise](./indicators.md)
- [Findings & Defense Actions](./findings.md)
