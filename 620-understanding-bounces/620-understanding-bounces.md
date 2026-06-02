# Understanding Bounces

**

In this article:

- [Introduction to bounces](#Introduction-to-bounces-aPeKp)

- [Potential recipient bounce issues](#Potential-recipient-bounce-issues-1TnFB)

- [Potential sender bounce issues](#Potential-sender-bounces-LkioY)

## Introduction to bounces

Bounces can negatively affect the deliverability of your emails, but understanding why they happen is the first step to solving the problem.

Bounces occur when emails can't be delivered due to various issues, and unfortunately, this is something we don't have control over in QuickMail. The only way to verify and address bounces is by checking the bounced email notification, which can be found directly in your inbox.

**

Here are some of the most common reasons emails bounce and how to fix them:

## Potential recipient bounce issues

### Recipient email address doesn't exist / Invalid Recipient / Address not found

This bounce occurs because the recipient's email address is either misspelled, no longer active or doesn't exist at all, preventing the email from being delivered.

### Solution:

Verify leads before sending emails. This way, invalid email addresses will be filtered. Here's a step-by-step guide on how email verification works in QuickMail: Verifying Leads

There are other recipient bounces that can't be predicted, for example:

550: Blocked by Policy** – The recipient’s email server blocked the message due to their filtering policy. This can happen if your IP is blacklisted or the recipient’s server blocks certain domains or IP addresses.

**552: Mailbox Full** – The recipient’s inbox has exceeded its storage limit.

**554: Message Rejected** – The recipient’s server rejected the message, often due to spam filters or domain reputation issues.

**451: Temporary Server Problem** – The recipient’s server is experiencing temporary issues and is not accepting emails.

**

## Potential sender bounces

Sender-related bounces occur when issues on your end prevent your emails from reaching recipients. These can include:

•Poor Sending Reputation**: Your domain or IP address may have been flagged for spammy behavior.

•**Authentication Issues**: Misconfigured SPF, DKIM, or DMARC records can cause your emails to be rejected.

•**High Volume or Speed**: Sending too many emails too quickly can trigger rate limits or blacklisting.

**

For detailed fixes on these issues, refer to our Fixing Bounces Guide**.

-
