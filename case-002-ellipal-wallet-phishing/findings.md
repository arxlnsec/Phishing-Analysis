# Findings & Recommendations

## Verdict

This is a sophisticated phishing attack impersonating ELLIPAL Wallet using domain typosquatting (ellipalwallet.io vs. ellipal.com), email service abuse (BIGLOBE infrastructure), and social engineering tactics. The fake "Desktop Wallet" software does not exist and is designed to steal cryptocurrency credentials or install credential-stealing malware. The malicious domain has been confirmed as malicious by multiple security vendors (VirusTotal: 13/91, Hybrid-Analysis: 2/6 malicious + 1 suspicious, Sandbox: 90/100 threat score). This represents a high-risk threat to cryptocurrency users.

## Key Findings

- Attacker impersonates ELLIPAL Wallet, a legitimate cryptocurrency hardware wallet provider
- Falsely advertises non-existent "ELLIPAL Desktop Wallet" application
- Uses domain typosquatting technique (ellipalwallet.io vs. legitimate ellipal.com)
- Leverages legitimate BIGLOBE email service infrastructure to bypass authentication filters
- No legitimate connection between BIGLOBE/KDDI and ELLIPAL Wallet
- Malicious domain confirmed by 13/91 vendors on VirusTotal
- High threat score (90/100) from sandbox analysis
- Targets cryptocurrency users who may be less cautious about downloading wallet software
- Primary objective: credential harvesting (seed phrases, private keys)

## Defense Actions

### Immediate Actions
- Block the malicious domain ellipalwallet.io at DNS level, email gateway, and firewall
- Block the sender email xa6yw6@bma.biglobe.ne.jp at email gateway
- Quarantine all emails containing links to ellipalwallet.io
- Alert all users, especially cryptocurrency holders, about this phishing campaign
- Report malicious domain and sender to BIGLOBE abuse contacts for investigation

### Detection & Prevention
- Create email rule to detect similar domain typosquatting patterns (ellipal + wallet variations)
- Implement URL filtering to block ellipalwallet.io and similar variants
- Monitor for emails impersonating legitimate cryptocurrency wallet providers
- Flag emails claiming to introduce new desktop/mobile applications from hardware wallet manufacturers (which typically don't release desktop software)
- Create detection rule for emails impersonating cryptocurrency providers

### User Education
- Educate users that ELLIPAL only manufactures hardware wallets, not desktop applications
- Remind users to always verify domain names carefully before downloading cryptocurrency-related software
- Warn users never to share seed phrases or private keys via email or downloaded software
- Recommend downloading wallet software only from official websites (ellipal.com, not ellipalwallet.io)
- Provide list of legitimate cryptocurrency wallet provider domains to users

### Long-term Actions
- Monitor for similar phishing campaigns targeting other cryptocurrency wallet providers (Ledger, Trezor, etc.)
- Track domain registrations for typosquatting variations of legitimate wallet names
- Report findings to cryptocurrency security communities and ELLIPAL directly
- Implement enhanced email authentication requirements for cryptocurrency-related communications
- Maintain database of known phishing domains targeting cryptocurrency users
