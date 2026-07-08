# URL Analysis

## Malicious Domain

**Malicious Domain:** ellipalwallet.io  
**Legitimate Domain (Impersonated):** ellipal.com  
**Attack Type:** Domain typosquatting

The attacker registered "ellipalwallet.io" (using .io TLD instead of .com) as a domain typosquatting technique, banking on users not carefully verifying the domain before downloading software. The visual similarity between ellipalwallet.io and the legitimate ellipal.com is intentional, users may quickly see "ellipal" and "wallet" and trust the domain.

## Malicious URL

**URL:** https://www.ellipalwallet.io/

This URL is embedded in the email and directs users to the fake domain where they are likely presented with:
- Credential harvesting forms (seed phrase/private key input)
- Malicious software downloads
- Fake wallet interface designed to steal credentials

## Security Vendor Detection

**VirusTotal Analysis:**
- Detection Rate: 13/91 security vendors flagged as malicious
- Verdict: Confirmed phishing/malware domain

**Hybrid-Analysis Detection:**
- Malicious: 2/6 antivirus tools
- Suspicious: 1/6 antivirus tools
- Total detection: 3/6 tools flagged concerns

**Sandbox Analysis:**
- Threat Score: 90/100
- Classification: Malicious
- Verdict: Confirmed threat

## Domain Registration Details

- **Registered Domain:** ellipalwallet.io
- **Typosquatting Target:** ellipal.com
- **Visual Similarity:** High (intentional resemblance to legitimate domain)
- **Likelihood of User Error:** High (users may not notice .io vs .com difference)

## Attack Flow

1. User receives email claiming ELLIPAL Desktop Wallet is available
2. User clicks link to https://www.ellipalwallet.io/
3. User lands on fake ELLIPAL website
4. User is prompted to enter seed phrase, private key, or wallet credentials
5. Credentials are captured by attacker
6. Attacker gains access to cryptocurrency holdings

## Verdict

Confirmed malicious domain designed to harvest cryptocurrency credentials (seed phrases, private keys, or wallet login credentials). Multiple security vendors and sandbox analysis confirm the domain is hosting malicious content or credential harvesting forms.
