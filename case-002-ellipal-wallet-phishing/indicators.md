# Indicators of Compromise (IOCs)

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

## Sender Indicators
- **Malicious Email Address:** xa6yw6@bma.biglobe.ne.jp
- **Spoofed Organization:** ELLIPAL Wallet
- **Email Service Provider:** BIGLOBE (Japanese ISP, owned by KDDI Corporation)
- **Sender IP:** 27.86.113.9
- **Resolved Host:** mta-snd-e09.biglobe.ne.jp
- **Mail Server:** BIGLOBE Mail Transfer Agent

## Primary Domain Indicators
- **Primary Malicious Domain:** ellipalwallet.io
- **Legitimate Domain (Impersonated):** ellipal.com
- **Attack Type:** Domain typosquatting (.io vs .com)
- **VirusTotal Detection:** 13/91 security vendors flagged as malicious
- **Hybrid-Analysis Detection:** 2/6 malicious, 1/6 suspicious
- **Sandbox Analysis:** 90/100 threat score, flagged as malicious
- **Purpose:** Landing page that redirects to secondary malicious domain

## Secondary Domain Indicators
- **Secondary Malicious Domain:** ellipalpcpro.com
- **Purpose:** Malware distribution (hosts malicious desktop application download)
- **Relationship:** Contacted by ellipalwallet.io during sandbox analysis
- **Attack Chain:** ellipalwallet.io → ellipalpcpro.com
- **Sandbox Evidence:** Screenshots show download functionality for malicious desktop application

## URL Indicators
- **Primary URL:** https://www.ellipalwallet.io/
- **Secondary URL:** https://www.ellipalpcpro.com/

## Authentication Status
- **SPF:** PASS (legitimate BIGLOBE infrastructure)
- **DKIM:** PASS (legitimate BIGLOBE infrastructure)
- **DMARC:** PASS (legitimate BIGLOBE infrastructure)
- **Note:** Authentication passes due to email service abuse; attacker using legitimate BIGLOBE email servers

## Recommendation
Block both malicious domains (ellipalwallet.io and ellipalpcpro.com) at DNS, email gateway, and firewall level. Flag sender email xa6yw6@bma.biglobe.ne.jp or BIGLOBE service provider for abuse. Monitor for traffic to either domain.
