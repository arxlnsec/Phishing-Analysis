# URL Analysis

## Primary Malicious Domain

**Malicious Domain:** ellipalwallet.io  
**Legitimate Domain (Impersonated):** ellipal.com  
**Attack Type:** Domain typosquatting

The attacker registered "ellipalwallet.io" (using .io TLD instead of .com) as a domain typosquatting technique, banking on users not carefully verifying the domain before downloading software. The visual similarity between ellipalwallet.io and the legitimate ellipal.com is intentional—users may quickly see "ellipal" and "wallet" and trust the domain.

## Primary Malicious URL

**URL:** https://www.ellipalwallet.io/

This URL is embedded in the email and directs users to a landing page that acts as the first stage of a two-stage infection chain. The landing page appears legitimate but is actually designed to redirect users to a secondary malicious domain.

## Secondary Malicious Domain

**Secondary Domain:** ellipalpcpro.com  
**Relationship:** Contacted by ellipalwallet.io during sandbox analysis  
**Purpose:** Malware distribution (hosts malicious desktop application for download)

According to sandbox analysis, the malicious domain ellipalwallet.io contacts another malicious domain ellipalpcpro.com. The sandbox traffic analysis and screenshots reveal that ellipalwallet.io acts as a landing page that redirects or directs users to ellipalpcpro.com, which is the actual site hosting the malicious "ELLIPAL Desktop Wallet" application for download. This two-stage infection chain suggests a more sophisticated attack where the initial phishing email leads to a seemingly legitimate landing page (ellipalwallet.io) that then distributes the actual malware payload from a secondary domain (ellipalpcpro.com).

**Sandbox Evidence:**
- Sandbox screenshots show download functionality on ellipalpcpro.com
- Traffic analysis confirms connection from ellipalwallet.io to ellipalpcpro.com
- Both domains are confirmed malicious by security vendors
- Secondary domain hosts the actual malicious desktop application executable

## Secondary Malicious URL

**URL:** https://www.ellipalpcpro.com/

This URL hosts the malicious "ELLIPAL Desktop Wallet" application download. Users who download and execute this file will have their cryptocurrency credentials compromised or malware installed on their systems.

## Security Vendor Detection - Primary Domain

**VirusTotal Analysis (ellipalwallet.io):**
- Detection Rate: 13/91 security vendors flagged as malicious
- Verdict: Confirmed phishing/malware domain

**Hybrid-Analysis Detection (ellipalwallet.io):**
- Malicious: 2/6 antivirus tools
- Suspicious: 1/6 antivirus tools
- Total detection: 3/6 tools flagged concerns

**Sandbox Analysis (ellipalwallet.io):**
- Threat Score: 90/100
- Classification: Malicious
- Verdict: Confirmed threat

## Domain Registration Details

**Primary Domain (ellipalwallet.io):**
- Registered Domain: ellipalwallet.io
- Typosquatting Target: ellipal.com
- Visual Similarity: High (intentional resemblance to legitimate domain)
- Likelihood of User Error: High (users may not notice .io vs .com difference)

## Attack Flow

1. User receives email claiming ELLIPAL Desktop Wallet is available
2. User clicks link to https://www.ellipalwallet.io/
3. User lands on landing page appearing to be legitimate ELLIPAL site
4. Landing page redirects to https://www.ellipalpcpro.com/
5. User is presented with download option for malicious "Desktop Wallet" application
6. User downloads and executes the malicious application
7. Malware installs on system or credential harvesting form steals wallet information
8. Attacker gains access to cryptocurrency holdings or installs persistent malware

## Verdict

Confirmed sophisticated two-stage malicious infrastructure designed to harvest cryptocurrency credentials or distribute malware. The primary domain (ellipalwallet.io) acts as a landing page that directs users to a secondary domain (ellipalpcpro.com) hosting the actual malware payload. Multiple security vendors have confirmed both domains as malicious through detection, analysis, and sandbox execution.
