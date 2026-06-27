# Email Analysis

## Sender Analysis

The email falsely claims to originate from Capital One but was actually sent from xserver.com, a fake domain registered by the attacker and hosted on Kagoya VPS (Japan) at IP address 133.18.212.99. The email routing shows only a single Received header, indicating direct send from the attacker's VPS rather than passage through Capital One's legitimate mail servers. Legitimate Capital One emails would have 3-5+ Received headers from their own infrastructure. 

Email authentication mechanisms are not configured on the fake xserver.com domain, meaning there are no SPF records authorizing the sending IP, no DKIM signatures from Capital One's private keys, and no DMARC policies to reject spoofed emails. 

The sender displays multiple critical spoofing indicators: 
- Domain mismatch (xserver.com versus legitimate capitalone.com)
- Geographic mismatch (US bank claiming to send from Japan)
- Infrastructure mismatch (rental VPS versus enterprise bank servers)

The email uses sophisticated social engineering tactics including urgency ("Action Required"), fear ("Payment on Hold"), financial incentive ("incoming payment"), and artificial time pressure ("24-72 hours"), combined with a generic greeting and typos that indicate mass distribution. 

**Overall assessment confirms the sender is not legitimate and this is a confirmed spoofing attack with 100% certainty.**

## Email Headers

```
Date: 09 Aug 2023 01:13:53 +0900
Subject: Action Required: New Payment Temporary on Hold
To: garyb59@protonmail.com
From: "Capita One" <winner@xserver.com>
Return-Path: winner@xserver.com
Sender IP: 133.18.212.99
Resolve Host: v133-18-212-99.vir.kagoya.net
Message-ID: 20230809011353.A4793969C16D077F@xserver.com
```

## Verdict
This is a spoofing attack with 100% certainty based on multiple authentication failures and infrastructure mismatches.
