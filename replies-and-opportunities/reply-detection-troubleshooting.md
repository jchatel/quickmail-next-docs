# Troubleshooting Reply Detection in QuickMail

## How Reply Detection Works

QuickMail embeds a tracking code in every email sent through the platform. Every 10 minutes, QuickMail scans all folders in the connected inbox (except the Sent folder) looking for emails that contain this tracking code. When a match is found, the lead is automatically marked as replied and their journey is stopped — no further follow-up emails will be sent to them from that campaign.

---

## Why a Reply Might Not Be Detected

### 1. Limited inbox access
Third-party apps like QuickMail may not have full access to the inbox depending on how permissions were granted during setup.

### 2. Hidden reply folder
If the folder where replies are saved is hidden, QuickMail won't be able to scan it.

### 3. Reply came from a different email address
QuickMail looks for replies from the exact email address added as a lead. If the lead replies from a different address (e.g., lead added as `xyz@xyz.com` but reply came from `x.yz@xyz.info`), the reply may not be matched — though QuickMail can often still detect it via the tracking code.

### 4. Tracking code stripped by the email app
Some email apps strip tracking codes from replies. When this happens, QuickMail can't associate the reply with the correct lead. This is outside QuickMail's control.

### 5. Reply deleted before detection
If the reply is deleted from the inbox before the 10-minute scan runs, QuickMail won't be able to detect it.

### 6. Incorrect MX records
If the MX records for the inbox are misconfigured, replies may not route correctly.

---

## Replies from Aliases

If a lead replies using an alias not added to the account, QuickMail can usually still detect the reply — but if the email app strips the tracking code, detection will fail.

Since QuickMail has no control over the lead's email settings, the recommended solution is to enable **company-wide reply monitoring**.

### How company-wide reply monitoring works

When this setting is enabled:
- QuickMail automatically creates a lead for the alias
- All leads under the same domain are marked as replied

This removes the need to manually track and mark leads as replied.

> **Note:** If your team is contacting free email domains (e.g., gmail.com), enabling this setting may cause unrelated leads to be marked as replied since they share the same domain.

---

## Manually Marking a Journey as Replied

If a reply wasn't detected and you need to stop follow-ups immediately, mark the journey as replied manually:

1. Click the **lead's thumbnail**
2. Go to the **Campaigns** section
3. Click the **triple-dot icon** next to the lead
4. Select **Set as Replied**

---

## Reply Detection: Same Domain vs. Different Domain

QuickMail can detect a reply if it comes from the same domain as the lead and **Treat replies as company-wide** is enabled.

| Scenario | Detected? |
|---|---|
| Lead: `peter@mycompany.com` replies as `peter.s@mycompany.com` | Yes — same domain |
| Lead: `peter@mycompany.com` replies from `peter@anotherdomain.com` | Unlikely — different domain |

---

## How QuickMail Tracks Replies

QuickMail uses three methods to identify replies:

- The **email address** of the lead
- A **tracking pixel** embedded in the sent email
- **Metadata** included in the original email

If a lead sends a brand-new email from a different address instead of replying directly to the campaign email, that message won't contain the tracking pixel or metadata — and QuickMail won't recognize it as a reply.

---

## Is a Reply Not Being Detected in QuickMail?

If you've confirmed a reply was sent but it isn't showing up, work through the checklist above to identify the most likely cause. If the issue persists, reach out to support with the lead's email address, the campaign name, and the approximate time the reply was sent.
