# Indicators of Compromise (IOCs)

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

## Sender Indicators
- **Malicious Domain:** xserver.com
- **Sender Email:** winner@xserver.com
- **Spoofed Organization:** Capital One
- **Sender IP:** 133.18.212.99
- **Resolved Host:** v133-18-212-99.vir.kagoya.net
- **Hosting Provider:** Kagoya VPS (Japan)

## Authentication Indicators
- **SPF Records:** Not configured
- **DKIM Signatures:** None
- **DMARC Policy:** None configured

## Attachment Indicators
- **Filename:** Secure_Payment_CapitalOne_Accont.html
- **MD5:** 2645deb7d2368c7ce87593e0d6c592f6
- **SHA1:** 65af7bfdbe8c68e8eb9b3b8e07c46033ccd84bef
- **SHA256:** 99edbec6dd4df95330ef8d0c14a5ff9a5b4ee066fbcdb1d5f57134398e8882f7
- **File Type:** HTML with embedded JavaScript
- **VirusTotal Detection:** 16/62 security vendors flagged as malicious

## Recommendation
Block all indicators at email gateway, firewall, and SIEM level.
