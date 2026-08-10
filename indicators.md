# Indicators of Compromise (IOCs)

## Email Headers

Date: Sat, 8 Mar 2025 18:23:32 +0000
Subject: Elon Musk's ESaver Giveaway - Don't Miss Out!
From: ESaver x Elon Musk <info@zhishangmingzhan.com>
To: Undisclosed recipients:;
Return-Path: info@zhishangmingzhan.com
Sender IP: 135.224.5.224
Resolve Host: 73jg.kyfishermen.co.uk
Message-ID: <xvvxnqr.buewkp.ohse@ssavgcwh.com>

## Sender Indicators
- **Malicious Email Address:** info@zhishangmingzhan.com
- **Spoofed Organization:** ESaver x Elon Musk (fake brand)
- **Sender Domain:** zhishangmingzhan.com
- **Return-Path:** info@zhishangmingzhan.com
- **Sender IP:** 135.224.5.224
- **Resolved Host:** 73jg.kyfishermen.co.uk
- **IP Geolocation:** United States (Melrose Park, Microsoft)
- **IP Owner:** Microsoft Corporation (AS8075 - MSN AS Block)
- **Attack Method:** Abuse of Microsoft cloud infrastructure

## Domain Indicators
- **Malicious Domain:** metaverseshades.com
- **Sender Domain:** zhishangmingzhan.com
- **VirusTotal Detection (metaverseshades.com):** 11/92 security vendors flagged as malicious/phishing
- **Vendors Flagged as Malicious:** ADMINUSLabs, BitDefender, CyRadar, Fortinet, Lionic, Webroot
- **Vendors Flagged as Phishing:** ADMINUSLabs, BitDefender, CyRadar, Fortinet, Sophos
- **Threat Type:** Phishing/credential harvesting

## URL Indicators
- **Primary Malicious URL:** http://metaverseshades.com/gjqrw.php?32=e1fb1c96f75f167c3_12f1.bf8aab2.803f445795156d02a9_56aa7e.6Z0vYd7vrBck0750r7v5vvp0rvvY0MYdY057xYMr
- **Secondary Malicious URL:** http://metaverseshades.com/vvobj.php?32=39a4669800fef4567_e191.64b5100.6139cde663af1ed337_e41912.n40vYd7vrBck0750r7v5vvp0rvvY0MYdY057xYMr
- **URL Placement:** Embedded in email images and hyperlinked text
- **Parameter Type:** Heavily obfuscated tracking/redirector parameters
- **Protocol:** HTTP (unencrypted)

## Authentication Status
- **SPF:** PASS (sender IP 135.224.5.224 designated as permitted sender)
- **DKIM:** NONE (message not signed)
- **DMARC:** PERMERROR (permanent error in DMARC configuration)
- **Sender Score:** Questionable (passes SPF due to Microsoft infrastructure abuse)

## Campaign Characteristics
- **Target:** Undisclosed recipients (mass mailing)
- **Impersonation:** Celebrity (Elon Musk) and fake product (ESaver)
- **Message Priority:** High (X-Priority: 1, Importance: high)
- **Subject Line:** Celebrity/authority + giveaway theme
- **Email Type:** HTML email with embedded image links
- **Message ID:** Randomized (xvvxnqr.buewkp.ohse@ssavgcwh.com)

## Scam Claims
- ESaver is Elon Musk's "new electricity saving invention"
- Up to 90% reduction in monthly electric bills
- Limited time "exclusive" offer
- "Congratulations, You Have Won" messaging
- Target audience: Illinois residents (mentioned in email)

## Recommendation
Block sender domain zhishangmingzhan.com at email gateway. Block access to metaverseshades.com at network and DNS level. Monitor for similar celebrity impersonation phishing campaigns. Report Microsoft IP abuse (135.224.5.224) to Microsoft security team for investigation and potential account suspension.
