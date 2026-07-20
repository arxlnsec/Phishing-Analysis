# Email Analysis

## Sender Analysis

The email falsely claims to originate from "Perfect Gifts Of 2025" but was actually sent from renewcnzlac@wlodmbvsouyasilha.com, a suspicious sender domain with obfuscated naming that bears no legitimate relationship to holiday gift retail. The sender IP (13.84.221.57) resolves to Microsoft Corporation infrastructure (MSN Block), indicating the attacker is abusing legitimate cloud infrastructure to send phishing emails and bypass email filters.

The authentication results reveal a concerning pattern: SPF passes because the sending IP (13.84.221.57) is legitimately designated as a permitted sender by Microsoft. However, DKIM is absent (no cryptographic signature) and DMARC returns a permanent error. This combination suggests the attacker is leveraging Microsoft's infrastructure either through a compromised account or a misconfigured cloud service to send mass phishing emails. The routing through multiple Outlook servers (MW4PR10MB5749, CH3PR10MB7630, DM5PR08CA0059) shows the email passed through legitimate Microsoft filtering, which explains why it passed SPF authentication—it actually originated from Microsoft infrastructure.

The "To" field lists only "Undisclosed recipients:;" confirming this is a mass mailing campaign sent to a large recipient list that was not disclosed to other recipients. This is typical of spam and phishing campaigns designed to reach maximum recipients while obscuring the actual targeting.

The email headers also reveal suspicious X-headers: X-Priority is set to 1 (high), and Importance is marked as "high"—social engineering tactics designed to make users treat this as urgent communication requiring immediate action.

## Subject Line Analysis

**Subject:** "31 awesome, affordable gifts perfect for xmas this year"

**Social Engineering Tactics:**
- Seasonal exploitation: Targets users distracted by holiday shopping
- Urgency through specificity: "31 awesome" creates FOMO (fear of missing out)
- Price appeal: "affordable gifts" exploits budget-conscious shopping behavior
- Timeliness: "perfect for xmas this year" creates sense of immediacy (limited time offer)
- Casual, conversational tone: Mimics legitimate retail marketing

The subject line is deliberately generic and non-branded, allowing it to appeal to a broad audience without raising immediate suspicion that a specific brand is being impersonated.

## Email Body Analysis

The email body contains minimal text and relies heavily on embedded images with clickable links. All user engagement points (headings, images) contain the same malicious URL embedded as clickable links. This technique is designed to obscure the true destination URL from email filters and reduce the likelihood of URL scanning by sandboxing engines (images are harder to analyze than plain text links).

The email uses multiple image sources (https://i.imgur.com for legitimate image hosting) which may be an attempt to further evade filtering by mixing legitimate image services with malicious links.

## Verdict

Confirmed mass phishing attack using spoofed sender identity, obfuscated malicious URLs, and exploitation of legitimate Microsoft infrastructure. The attacker uses generic holiday branding rather than impersonating a specific company, suggesting this is a high-volume campaign designed for maximum delivery and user engagement. The heavy reliance on embedded image links indicates sophistication in evading email gateway filtering.
