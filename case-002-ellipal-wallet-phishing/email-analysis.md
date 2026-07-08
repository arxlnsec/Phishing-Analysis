# Email Analysis

## Sender Analysis

The email falsely claims to originate from "ELLIPAL WALLET" but was actually sent from xa6yw6@bma.biglobe.ne.jp, an email address registered with BIGLOBE, a Japanese Internet Service Provider owned by KDDI Corporation. The sender uses a legitimate email service infrastructure, which explains why SPF, DKIM, and DMARC authentication checks pass—BIGLOBE's legitimate email servers are properly configured for these protocols. However, this is a case of email service abuse where the attacker registered an account with a legitimate provider to bypass security filters.

The resolved host (mta-snd-e09.biglobe.ne.jp) confirms the email was sent through BIGLOBE's mail transfer agents. There is no legitimate connection between BIGLOBE/KDDI Corporation and ELLIPAL Wallet, confirming this is a spoofed sender impersonating an official ELLIPAL communication. The use of a legitimate Japanese email service combined with sender spoofing creates a convincing appearance of legitimacy, increasing the likelihood that recipients will trust the email and click the malicious link.

## Email Headers

```
Date: Thu, 16 Apr 2026 02:52:32 +0000
Subject: ELLIPAL Desktop Wallet is here - Manage your portfolio from Windows and macOS
To: phishing@pot
From: ELLIPAL WALLET <xa6yw6@bma.biglobe.ne.jp>
Return-Path: xa6yw6@bma.biglobe.ne.jp
Sender IP: 27.86.113.9
Resolve Host: mta-snd-e09.biglobe.ne.jp
Message-ID: <97c5d8ca-72b7-8dde-27a5-35c800fff8cb@bma.biglobe.ne.jp>
```

## Subject Line Analysis

**Subject:** "ELLIPAL Desktop Wallet is here - Manage your portfolio from Windows and macOS"

**Social Engineering Tactics:**
- Urgency: "is here" (implies new product launch)
- Feature appeal: "Manage your portfolio" (attractive to cryptocurrency users)
- Platform availability: "Windows and macOS" (appears legitimate and widely accessible)
- Generic announcement style (mimics legitimate software product releases)

The subject is designed to make cryptocurrency users believe ELLIPAL has released an official desktop application, when in reality ELLIPAL only manufactures hardware wallets and has no desktop software.

## Verdict

Confirmed spoofing attack using compromised/abused legitimate email infrastructure (BIGLOBE). The attacker leveraged a legitimate email service to make the phishing email appear credible and bypass email authentication filters.
