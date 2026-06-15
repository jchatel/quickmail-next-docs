# Deliverability Report

**In this article:**

- Why keep track of the Deliverability Report?

- How does it work?

- How to receive a weekly Deliverability Report?

- How to manually generate a Deliverability Report?

- Analyzing the Deliverability Report

- How can I improve the deliverability of my inbox?

## Why Keep Track of the Deliverability Report?

The Deliverability Report shows where emails from an email account are landing — inbox, spam, or promotions. It also shows whether your SPF and DKIM records are configured correctly. Knowing where your emails are landing helps you quickly identify and resolve deliverability issues.

## How Does It Work?

When deliverability testing is enabled, QuickMail automatically sends occasional test emails from your connected email account to monitored inboxes. These tests occur after the email account is first added, and then at the start of each week going forward.

You may see messages in your Sent Items that you do not recognize, sent to unfamiliar recipients. This is normal — it is QuickMail testing the deliverability of your email account and does not mean your account has been compromised.

Here are some examples of recipient names used in test emails:

- Everlyne

- Everlyne Green

- Richard

- Richard Hendricks

- noreply

- qmnorep

Here are some examples of subject lines used in test emails:

- Coffee next Monday?

- Meeting Next Wednesday?

- Hi from (yourname)

- Everlyne Green / (yourname)

- Quick question Everlyne Green?

## How to Receive a Weekly Deliverability Report?

To receive a weekly Deliverability Report for a specific email account, go to **Channels** → **Email** → click the email account → **Deliverability** tab → check **Automatically test deliverability of this inbox each week**.

## How to Manually Generate a Deliverability Report?

To manually generate a Deliverability Report at any time, go to **Channels** → **Email** → click the email account → **Deliverability** tab → click **Generate Report**.

**Note:** It may take up to 30 minutes for the report to generate.

## Analyzing the Deliverability Report

### SPF

If the SPF test fails, there is an issue with the email account's SPF record. You can use [MxToolbox](https://mxtoolbox.com/) to identify the cause.

Common SPF errors and how to fix them:

- **Multiple SPF records** — having more than one SPF record is not allowed. Delete the duplicate records or merge them into a single SPF record.

- **SPF deprecated** — the SPF DNS record type was discontinued in 2014. Change the SPF record to a TXT DNS type.

- **Wrong SPF syntax** — if the email account is from Google or Outlook, follow this guide: SPF, DKIM, and DMARC Records. For other email providers, check their documentation or contact their support team.

### DKIM

Only one email provider's DKIM is tested per deliverability report. It is normal to see DKIM shown in yellow as "Skipping test."

### Delivered to: Inbox

If the test email successfully lands in the monitored inbox, the result will show "Delivered to Inbox." This is a good indication that your emails are likely reaching the inbox of that email provider.

### Delivered to: Spam

If the test email lands in spam, the result will show "Delivered to Spam." It is normal for emails from new email accounts to land in spam, especially when the recipient uses Outlook.

## How Can I Improve the Deliverability of My Email Account?

Emails can land in spam for several reasons, including the volume of emails sent, email content, the age of the email account, or DNS record configuration.

The following guides may help:

- [Ultimate Guide to Cold Email Deliverability](https://quickmail.com/cold-email-deliverability)

- [The Ultimate Cold Email Checklist](https://quickmail.com/checklist)

- [Cold Email: The Definitive Guide](https://quickmail.com/cold-email)
