# Adding SPF, DKIM, and DMARC Records

Proper email authentication protects your domain from spoofing and improves deliverability. This article explains the three core DNS records you need to set up — SPF, DKIM, and DMARC — and what each one does.

---

## Why email authentication matters

Without authentication records, anyone can send email that appears to come from your domain. This damages your sender reputation, reduces deliverability, and puts your recipients at risk of phishing attacks. Most modern email providers (Gmail, Outlook, Yahoo) use these records to decide whether to deliver, filter, or reject incoming mail.

---

## SPF (Sender Policy Framework)

### What it is

SPF is a DNS record that lists which mail servers are authorized to send email on behalf of your domain. When a receiving server gets an email from you, it checks your SPF record to confirm the sending server is on the approved list.

### Why it matters

Without SPF, spammers can forge your domain as the "From" address. SPF gives receiving servers a way to verify the email actually came from you.

### How to add it

Add a TXT record to your domain's DNS:

| Field | Value |
|-------|-------|
| Type | TXT |
| Name | @ (or your domain) |
| Value | `v=spf1 include:yourmailprovider.com ~all` |

**Common provider values:**

| Provider | Include value |
|----------|---------------|
| Google Workspace | `include:_spf.google.com` |
| Microsoft 365 | `include:spf.protection.outlook.com` |
| Mailchimp | `include:servers.mcsv.net` |

**Tail options:**

- `~all` — Soft fail. Suspicious mail is accepted but marked. Recommended when starting out.
- `-all` — Hard fail. Mail from unauthorized servers is rejected. Use this once you're confident your SPF record is complete.
- `+all` — Allows all. Never use this.

> **Note:** You can only have one SPF record per domain. If you send from multiple providers, combine them into one record: `v=spf1 include:_spf.google.com include:spf.protection.outlook.com ~all`

---

## DKIM (DomainKeys Identified Mail)

### What it is

DKIM adds a cryptographic signature to every outgoing email. The signature is generated using a private key on your mail server and verified by recipients using a public key published in your DNS.

### Why it matters

DKIM proves that the email content has not been tampered with in transit and that it genuinely originated from your domain. It also helps build sender reputation over time, which improves deliverability.

### How to add it

DKIM setup depends on your email provider. They will generate the keys and give you a TXT record to add to your DNS.

**General format:**

| Field | Value |
|-------|-------|
| Type | TXT |
| Name | `selector._domainkey.yourdomain.com` |
| Value | `v=DKIM1; k=rsa; p=YOUR_PUBLIC_KEY` |

The `selector` is a label chosen by your provider (e.g. `google`, `selector1`, `s1`).

**Where to enable DKIM:**

- **Google Workspace:** Admin Console → Apps → Google Workspace → Gmail → Authenticate email
- **Microsoft 365:** Security portal → Email & Collaboration → Policies → Email Authentication Settings → DKIM
- **Other providers:** Check your provider's documentation for the exact DNS record to add

### How to verify DKIM is working

Use [MXToolbox DKIM Lookup](https://mxtoolbox.com/dkim.aspx). Enter your domain and the selector provided by your mail provider. If a key is returned, DKIM is active.

You can also send a test email to [mail-tester.com](https://www.mail-tester.com) to see a full authentication report.

---

### BIMI (Brand Indicators for Message Identification)

BIMI is an extension that lets your brand logo appear next to emails in supported inboxes, including Gmail, Yahoo Mail, and Apple Mail.

#### Requirements

Before BIMI will work, you need:

1. A DMARC record with `p=quarantine` or `p=reject` at 100% enforcement (`pct=100`)
2. Your logo in SVG Tiny PS format
3. A publicly accessible URL hosting that logo
4. Optionally, a VMC (Verified Mark Certificate) — required for Gmail logo display

#### How to add a BIMI record

| Field | Value |
|-------|-------|
| Type | TXT |
| Name | `default._bimi.yourdomain.com` |
| Value | `v=BIMI1; l=https://yourdomain.com/logo.svg; a=https://yourdomain.com/vmc.pem` |

- `l=` is the URL of your SVG logo
- `a=` is the URL of your VMC certificate (omit if you don't have one yet)

#### SVG logo requirements

- Format: SVG Tiny PS (not standard SVG)
- Shape: Square or circular — no transparency
- Size: Recommended minimum 32×32px viewbox

> **Note:** BIMI is cosmetic and not required for email deliverability. Focus on SPF, DKIM, and DMARC first. Add BIMI once your DMARC policy is fully enforced.

---

## DMARC (Domain-based Message Authentication, Reporting & Conformance)

### What it is

DMARC ties SPF and DKIM together. It tells receiving servers what to do when an email fails SPF or DKIM checks — and sends you reports so you can monitor what's happening with your domain.

### Why it matters

DMARC gives you visibility and control. Without it, even with SPF and DKIM in place, there is no instruction for what to do with mail that fails authentication. DMARC also unlocks BIMI support and is increasingly required by major providers for bulk senders.

### How to add it

Add a TXT record to your DNS:

| Field | Value |
|-------|-------|
| Type | TXT |
| Name | `_dmarc.yourdomain.com` |
| Value | `v=DMARC1; p=none; rua=mailto:dmarc@yourdomain.com` |

### Key parameters

| Parameter | What it does | Example |
|-----------|--------------|---------|
| `p=` | Policy — what to do with failing mail | `none`, `quarantine`, `reject` |
| `pct=` | Percentage of mail the policy applies to | `pct=100` |
| `rua=` | Email address for aggregate reports | `rua=mailto:dmarc@yourdomain.com` |
| `ruf=` | Email address for forensic (failure) reports | `ruf=mailto:dmarc@yourdomain.com` |
| `sp=` | Policy for subdomains | `sp=reject` |

### Recommended rollout

Start with a monitor-only policy and tighten it gradually once you have confirmed your legitimate mail is passing authentication.

**Step 1 — Monitor (start here)**
```
v=DMARC1; p=none; rua=mailto:dmarc@yourdomain.com
```

**Step 2 — Quarantine (after reviewing reports)**
```
v=DMARC1; p=quarantine; pct=100; rua=mailto:dmarc@yourdomain.com
```

**Step 3 — Reject (full enforcement)**
```
v=DMARC1; p=reject; pct=100; rua=mailto:dmarc@yourdomain.com
```

> **Important:** Do not jump to `p=reject` without first reviewing DMARC reports. If any legitimate mail streams are missing SPF or DKIM alignment, they will be rejected.

### Reading DMARC reports

Reports arrive as XML files sent to the address in `rua=`. They are hard to read manually. Use a free tool like [DMARC Analyzer](https://www.dmarcanalyzer.com) or [Google Postmaster Tools](https://postmaster.google.com) to parse and visualize them.

---

## Summary

| Record | What it does | Required for deliverability |
|--------|--------------|----------------------------|
| SPF | Authorizes sending servers | Yes |
| DKIM | Signs email content | Yes |
| DMARC | Enforces SPF + DKIM and sends reports | Strongly recommended |
| BIMI | Displays brand logo in inbox | No (but requires DMARC enforcement) |

**Setup order:** SPF → DKIM → DMARC (`p=none`) → review reports → DMARC (`p=reject`) → BIMI (optional)

---

## Related articles
- [Setting up custom sending domain tracking](https://help.quickmail.com/deliverability/custom-domain-tracking-to-improve-deliverability/)
- [Understanding Bounces](https://help.quickmail.com/deliverability/understanding-bounces/)
