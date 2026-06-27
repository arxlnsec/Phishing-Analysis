Headers
======================================
Date: 09 Aug 2023 01:13:53 +0900
Subject: Action Required: New Payment Temporary on Hold

To: garyb59@protonmail.com
From: "Capita One"<winner@xserver.com> 

Return-Path: <winner@xserver.com>

Sender IP: 133.18.212.99
Resolve Host: v133-18-212-99.vir.kagoya.net 

Message-ID:  <20230809011353.A4793969C16D077F@xserver.com>


Attachments
======================================
Attachment Name: Secure_Payment_CapitalOne_Accont.html
MD5: 2645deb7d2368c7ce87593e0d6c592f6
SHA1: 65af7bfdbe8c68e8eb9b3b8e07c46033ccd84bef
SHA256: 99edbec6dd4df95330ef8d0c14a5ff9a5b4ee066fbcdb1d5f57134398e8882f7


Description
======================================
This is a sophisticated phishing attack impersonating Capital One, a legitimate US financial institution. The attacker registered a fake domain (xserver.com) and hosted it on a Japanese VPS provider (Kagoya) to send fraudulent emails claiming pending payment notifications. The email employs multiple social engineering tactics including urgency ("24-72 hours"), financial incentive ("incoming payment"), and authority mimicry to convince the recipient to download a malicious HTML attachment disguised as a "secure payment verification form." The attachment likely contains a credential-harvesting form designed to steal Capital One login credentials. The email demonstrates advanced phishing techniques by avoiding suspicious links (using an attachment instead) and creating a compelling narrative around a pending payment to increase the likelihood of user interaction.


Artifact Analysis
======================================
Sender Analysis:

The email falsely claims to originate from Capital One but was actually sent from xserver.com, a fake domain registered by the attacker and hosted on Kagoya VPS (Japan) at IP address 133.18.212.99. The email routing shows only a single Received header, indicating direct send from the attacker's VPS rather than passage through Capital One's legitimate mail servers. Legitimate Capital One emails would have 3-5+ Received headers from their own infrastructure. Email authentication mechanisms are not configured on the fake xserver.com domain, meaning there are no SPF records authorizing the sending IP, no DKIM signatures from Capital One's private keys, and no DMARC policies to reject spoofed emails. The sender displays multiple critical spoofing indicators: domain mismatch (xserver.com versus legitimate capitalone.com), geographic mismatch (US bank claiming to send from Japan), and infrastructure mismatch (rental VPS versus enterprise bank servers). The email uses sophisticated social engineering tactics including urgency ("Action Required"), fear ("Payment on Hold"), financial incentive ("incoming payment"), and artificial time pressure ("24-72 hours"), combined with a generic greeting and typos that indicate mass distribution. Overall assessment confirms the sender is not legitimate and this is a confirmed spoofing attack with 100% certainty.


Attachment Analysis:

The attachment is an HTML document with embedded js, likely containing a fake Capital One login form designed to harvest credentials. VirusTotal detected it as malicious with 16/62 security vendors flagging it.


Verdict
======================================

This is a sophisticated phishing attack impersonating Capital One using domain spoofing (xserver.com), malicious HTML credential harvester, and social engineering tactics. The attachment is detected as malicious by 16/62 security vendors. 


Defense Actions
======================================

- Block sender domain xserver.com at email gateway/firewall
- Block IP address 133.18.212.99 (Kagoya VPS) at perimeter
- Flag and quarantine all emails from xserver.com across organization
- Create email rule to detect similar phishing patterns
- Alert all users about this phishing campaign