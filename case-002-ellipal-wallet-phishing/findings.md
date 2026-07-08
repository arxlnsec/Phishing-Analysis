# Findings & Recommendations

## Verdict

This is a highly sophisticated phishing attack impersonating ELLIPAL Wallet using domain typosquatting (ellipalwallet.io vs. ellipal.com), email service abuse (BIGLOBE infrastructure), and coordinated malicious infrastructure. The primary landing page (ellipalwallet.io) directs users to a secondary malicious domain (ellipalpcpro.com) which hosts the actual malicious "ELLIPAL Desktop Wallet" application for download. The fake software is designed to steal cryptocurrency credentials (seed phrases, private keys) or install credential-stealing malware on victim systems. Both malicious domains have been confirmed as malicious by multiple security vendors (Primary domain VirusTotal: 13/91, Hybrid-Analysis: 2/6 malicious + 1 suspicious, Sandbox: 90/100 threat score). This represents a critical-risk threat to cryptocurrency users.

## Key Findings

- Attacker impersonates ELLIPAL Wallet, a legitimate cryptocurrency hardware wallet provider
- Falsely advertises non-existent "ELLIPAL Desktop Wallet" application
- Uses sophisticated two-stage attack infrastructure (primary landing page + secondary distribution site)
- Primary domain (ellipalwallet.io) uses domain typosquatting technique (vs. legitimate ellipal.com)
- Secondary domain (ellipalpcpro.com) hosts actual malware distribution
- Sandbox analysis reveals network communication between malicious domains
- Leverages legitimate BIGLOBE email service infrastructure to bypass authentication filters
- No legitimate connection between BIGLOBE/KDDI and ELLIPAL Wallet
- Primary malicious domain confirmed by 13/91 vendors on VirusTotal
- High threat score (90/100) from sandbox analysis
- Targets cryptocurrency users who may be less cautious about downloading wallet software
- Primary objective: credential harvesting (seed phrases, private keys) and malware distribution
- Attack shows signs of sophistication with separated infrastructure (landing page vs. distribution site)

## Defense Actions

### Immediate Actions
- Block both malicious domains (ellipalwallet.io AND ellipalpcpro.com) at DNS level, email gateway, and firewall
- Block the sender email xa6yw6@bma.biglobe.ne.jp at email gateway
- Quarantine all emails containing links to either ellipalwallet.io or ellipalpcpro.com
- Alert all users, especially cryptocurrency holders, about this multi-stage phishing campaign
- Report both malicious domains and sender to BIGLOBE abuse contacts for investigation
- Monitor network traffic for any attempts to contact either malicious domain

### Detection & Prevention
- Create email rule to detect similar domain typosquatting patterns (ellipal + wallet variations)
- Implement URL filtering to block both ellipalwallet.io and ellipalpcpro.com and similar variants
- Monitor for emails impersonating legitimate cryptocurrency wallet providers
- Flag emails claiming to introduce new desktop/mobile applications from hardware wallet manufacturers (which typically don't release desktop software)
- Create detection rule for emails impersonating cryptocurrency providers
- Monitor network for DNS queries to malicious domains even if email is blocked

### User Education
- Educate users that ELLIPAL only manufactures hardware wallets, not desktop applications
- Remind users to always verify domain names carefully before downloading cryptocurrency-related software
- Warn users never to share seed phrases or private keys via email or downloaded software
- Recommend downloading wallet software only from official websites (ellipal.com, not ellipalwallet.io or ellipalpcpro.com)
- Provide list of legitimate cryptocurrency wallet provider domains to users
- Educate about two-stage attacks and the dangers of following redirects from suspicious links
- Advise users to verify HTTPS certificates and check domain spelling carefully

### Long-term Actions
- Monitor for similar phishing campaigns targeting other cryptocurrency wallet providers (Ledger, Trezor, etc.)
- Track domain registrations for typosquatting variations of legitimate wallet names
- Report findings to cryptocurrency security communities and ELLIPAL directly
- Implement enhanced email authentication requirements for cryptocurrency-related communications
- Maintain database of known phishing domains targeting cryptocurrency users
- Investigate and track infrastructure provider (ellipalpcpro.com hosting provider) for pattern analysis
- Monitor for similar two-stage attack patterns in cryptocurrency phishing campaigns
