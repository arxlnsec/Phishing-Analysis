# Indicators of Compromise (IOCs)

## Email Headers
```
Date: Thu, 30 Oct 2025 09:03:51 +0000
Subject: 31 awesome, affordable gifts perfect for xmas this year
From: Perfect Gifts Of 2025 <renewcnzlac@wlodmbvsouyasilha.com>
To: Undisclosed recipients:;
Return-Path: return@wlodmbvsouyasilha.com
Sender IP: 13.84.221.57
Resolve Host: 8cym.anningSalons.eu.com
Message-ID: <gpsrxor.nelunp.dmpa@plrrfoyh.com>
X-Priority: 1
Importance: high
```

## Sender Indicators
- **Malicious Email Address:** renewcnzlac@wlodmbvsouyasilha.com
- **Spoofed Organization:** Perfect Gifts Of 2025 (generic, non-existent brand)
- **Sender Domain:** wlodmbvsouyasilha.com
- **Return-Path:** return@wlodmbvsouyasilha.com
- **Sender IP:** 13.84.221.57
- **Resolved Host:** 8cym.anningSalons.eu.com
- **IP Geolocation:** United States (San Antonio)
- **IP Owner:** Microsoft Corporation (MSN Block - 13.84.221.57)
- **Attack Method:** Abuse of legitimate Microsoft infrastructure

## Domain Indicators
- **Malicious Domain:** thempresident.com
- **Domain Status:** Offline (no longer resolving)
- **VirusTotal Detection:** 7/92 security vendors flagged as malicious
- **Vendors Flagged as Malicious:** ADMINUSLabs, Chong Lua Dao, Fortinet, Sophos
- **Vendors Flagged as Suspicious:** Gridinsoft
- **Threat Type:** Phishing/Credential harvesting

## URL Indicators
- **Primary Malicious URL:** http://thempresident.com/Q7c0rxdOrP1leqtckz77XPO/6Z/1RSFZqKlXLUX9MzbBC10GmpB/eY7M5Bck/wFDtQyo0QTNCvl2UuA0IVmMW/rrr/vExW7aBoT9DOpk9J2Ow5/rvdMexx/sCml9fhW7QJUiKQ0Fkqh/7vMMd/zJ5FyiKoDWFcjv92dPVYcm1cn/v5v7/YzZ51g6E2ztTrJ2AMPYa/57xYMr/fNBYklLBuVban1LRHTyx8/
- **URL Placement:** Embedded in email images and text headings
- **Parameter Type:** Obfuscated tracking/redirector parameters
- **Protocol:** HTTP (unencrypted)

## Authentication Status
- **SPF:** PASS (sender IP 13.84.221.57 designated as permitted sender)
- **DKIM:** NONE (message not signed)
- **DMARC:** PERMERROR (permanent error in DMARC configuration)
- **Sender Score:** Questionable (passes SPF due to Microsoft infrastructure abuse)

## Campaign Characteristics
- **Target:** Undisclosed recipients (mass mailing)
- **Recipient Count:** Potentially hundreds/thousands
- **Message Priority:** High (X-Priority: 1)
- **Subject Line:** Holiday/seasonal theme (exploits Christmas shopping season)
- **Email Type:** HTML email with embedded images and links
- **Message ID:** Randomized (gpsrxor.nelunp.dmpa@plrrfoyh.com)

## Recommendation
Block sender domain wlodmbvsouyasilha.com and return domain return@wlodmbvsouyasilha.com at email gateway. Block access to thempresident.com at network level (though domain is currently offline). Monitor for similar holiday-themed phishing campaigns. Report Microsoft IP abuse (13.84.221.57) to Microsoft for investigation.
