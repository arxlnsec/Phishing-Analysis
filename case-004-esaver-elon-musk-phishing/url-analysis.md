# URL Analysis

## Malicious Domain

**Malicious Domain:** metaverseshades.com  
**Associated Sender Domain:** zhishangmingzhan.com  
**Primary Purpose:** Credential harvesting and scam redirection  
**Domain Status:** Active but malicious

The domain metaverseshades.com shows no obvious connection to ESaver, Elon Musk, or legitimate electricity-saving products. This generic domain selection is typical of phishing campaigns that use disposable infrastructure designed to be deployed quickly, redirect users to scam pages, then abandoned once security vendors catch it.

## Malicious URLs

**Primary URL:** http://metaverseshades.com/gjqrw.php?32=e1fb1c96f75f167c3\_12f1.bf8aab2.803f445795156d02a9\_56aa7e.6Z0vYd7vrBck0750r7v5vvp0rvvY0MYdY057xYMr

**Secondary URL:** http://metaverseshades.com/vvobj.php?32=39a4669800fef4567\_e191.64b5100.6139cde663af1ed337\_e41912.n40vYd7vrBck0750r7v5vvp0rvvY0MYdY057xYMr

**Protocol:** HTTP (unencrypted, red flag)  
**URL Embedding:** Embedded in email image and hyperlinked text for evasion  
**Parameter Obfuscation:** Heavily obfuscated parameters with tracking identifiers

The URLs use heavily obfuscated parameters that serve multiple purposes:

* Evade simple URL filtering based on domain patterns
* Track which emails led to user clicks and which links were clicked
* Likely redirect to different phishing/scam pages based on user characteristics
* Make manual URL verification by users more difficult

## Security Vendor Detection

**VirusTotal Analysis (metaverseshades.com):**

* Detection Rate: 11/92 security vendors flagged as malicious
* Verdict: Confirmed phishing and malware domain

**Vendors Flagging as Malicious:**

* ADMINUSLabs: Malicious
* BitDefender: Phishing
* CyRadar: Phishing
* Fortinet: Phishing
* Lionic: Malicious
* Webroot: Malicious

**Vendors Flagging as Phishing:**

* ADMINUSLabs: Phishing
* BitDefender: Phishing
* CyRadar: Phishing
* Fortinet: Phishing
* Sophos: Phishing

**Analysis Notes:** Multiple antivirus vendors specifically categorizing this as phishing (not just malware) indicates the domain hosts credential harvesting forms or phishing pages rather than direct malware distribution.

## Attack Flow

1. User receives email claiming Elon Musk is running an ESaver giveaway
2. Email uses celebrity authority and urgency ("Don't Miss Out")
3. Email claims user has already won the device ("Congratulations")
4. User sees comparison of $251/month to $15/month electric bills
5. User clicks link embedded in image (bypasses text-based URL filtering)
6. Browser navigates to http://metaverseshades.com/ with tracking parameters
7. Attacker's server identifies user location, device, and browser
8. User is likely presented with:

   * Fake ESaver order form requesting personal information
   * Payment processing for fake product
   * Redirection to secondary scam pages (pay-per-click schemes)
   * Identity theft harvesting forms

## URL Analysis Summary

The URLs demonstrate sophisticated phishing infrastructure:

* **Obfuscation:** Tracking parameters designed to be different for each user/email
* **Embedding:** Image-based links evade URL filters
* **Dynamic routing:** Backend PHP scripts likely route users based on parameters
* **Multiple endpoints:** gjqrw.php and vvobj.php suggest different campaigns or A/B testing

## Verdict

Confirmed sophisticated phishing domain confirmed by 11/92 security vendors. The heavily obfuscated URLs, embedded image links, and dynamic backend routing indicate professional phishing infrastructure designed for maximum user capture and data harvesting. The use of celebrity impersonation and false product claims combined with technical sophistication indicates this is likely run by organized phishing-as-a-service operation.

