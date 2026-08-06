**PhishGuard — Phishing Awareness Analysis Tool**
*Developed by Ateeq ur Rehman · DecodeLabs Project 3*

PhishGuard is an offline, browser-based tool that detects phishing across emails, messages, and URLs. It turns raw email text into a scored, explainable threat report by identifying suspicious links and keywords, flagging red flags, and explaining why a message is unsafe.

**Detection Engine**
- **Sender analysis:** Parses headers (From, Reply-To, Return-Path, Authentication-Results) to catch display-name spoofing, free-mail brand impersonation, Reply-To/Return-Path mismatches, and SPF failures.
- **Deep link analysis:** Breaks down URLs to detect IP-based links, punycode, the @-trick, shorteners (bit.ly, tinyurl), risky TLDs (.tk, .xyz), typosquatting via Levenshtein distance against 100+ brands, brand-in-subdomain tricks, homoglyphs, and mismatched visible vs. actual links.
- **Keyword engine:** Matches 15+ red-flag categories — urgency, threats, credential/data requests, money or gift-card/crypto pressure, prize scams, risky attachments, generic greetings, misspellings, hidden characters, base64 payloads, and scam phrasing.
- **Risk scoring:** Weighted indicators generate a 0–100 score with verdicts (Safe/Low/Medium/High/Critical); dangerous combinations boost scores and critical indicators escalate verdicts.

**Features**
- Email Analyzer (paste text or upload .eml/.txt, drag-and-drop)
- Link Scanner for standalone URL analysis with decoded parts
- Auto-generated red-flag checklist and reference sheet
- Reports explaining each flag's risk, a "Why is this unsafe?" summary, and print/JSON export
- 7 built-in samples (6 phishing types + 1 safe email)
- Strict mode toggle, fully offline, single dependency-free HTML file

**Verification**
All samples tested correctly — phishing emails scored High/Critical, safe emails scored 0/Safe, with no false positives on legitimate brand probes.

**Limitations**
As a heuristic, offline tool, it cannot expand shortened links, check DNS, or query domain reputation; .msg files aren't supported; folded headers are only partially parsed.

---
Word count: ~300. Want me to trim it further, adjust tone (more technical/more casual), or format it as a one-pager (PDF/DOCX) for your portfolio?
