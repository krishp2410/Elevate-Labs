# Phishing Email Analysis Report

## Overview

This project contains a detailed analysis of a real phishing email impersonating Spotify. The goal is to identify indicators of phishing to improve user awareness and email security literacy. The analysis covers email headers, content discrepancies, grammar issues, fake links, and security mismatches.

---

Important Note:  
- The phishing email analyzed in this report was actually received.  
- For privacy and security reasons:
  - The recipient’s email address has been changed to `tempmail@gmail.com`.  
  - The malicious domain, which is still active at the time of analysis, has been renamed to `www.phishspotify.com` instead of displaying the actual domain.

---

## Key Findings

### 1. Email Header Anomalies

| Field         | Value |
|---------------|-------|
| From          | Spotify Inc. `<spotify@sci-borg.co.uk, rajibdeb@revision.sci-borg.co.uk>` |
| To            | `<tempmail@gmail.com>` |
| Reply-To      | `<spotify@sci-borg.co.uk>` |
| IP Address    | `159.65.19.128 (no reverse DNS)` |
| Date          | Wed, 09 Apr 2025 02:44:51 UTC |
| Subject       | New login to Spotify |

Suspicious: Multiple unknown domains used (`@sci-borg.co.uk`, `@revision.sci-borg.co.uk`), no valid reverse DNS, inconsistent sender identity.

---

### 2. Threatening and Urgent Language

Examples from email body:
- “We noticed a new login on your account…”
- “If you don't recognize this login we recommend that you immediately Change your password…”

Used to create panic and prompt the user to act quickly without verification.

---

### 3. Malicious Link

| Displayed URL     | Actual Redirect |
|-------------------|-----------------|
| `www.spotify.com` | `www.phishspotify.com` |

Link text is misleading and redirects to a malicious domain.

---

### 4. Grammar and Typo Errors

| Sentence | Issue |
|----------|-------|
| “If you have signed in too your account lately…” | “too” should be “to” |
| “keep you account safe.” | “you” should be “your” |

Legitimate organizations proofread their emails; such errors are common in phishing.

---

### 5. Branding and UI Mismatches

- Incorrect sender display name and footer (e.g., “Spotify-team” instead of official support link)
- Missing Secure Account button
- Anchors do not lead to official Spotify pages

---

### 6. Timezone Inconsistency

- Expected Timezone: EDT (America)
- Used in Email: CET (used incorrectly for India instead of IST)

---

## Conclusion

This email is a phishing attempt.

Indicators of Phishing:

- Unknown sender domains
- Urgent and alarming language
- Mismatched/fake links
- Grammar errors
- Incorrect branding and timezone
- Lack of secure footer and verified IP

---