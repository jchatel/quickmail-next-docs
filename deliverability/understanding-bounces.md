# Understanding Bounces

In this article:

- Introduction to bounces

- Potential recipient bounce issues

- Potential sender bounce issues

## Introduction to bounces

Bounces can negatively affect the deliverability of your emails, but understanding why they happen is the first step to solving the problem.

Bounces occur when emails can't be delivered due to various issues, and unfortunately, this is something we don't have control over in QuickMail. The only way to verify and address bounces is by checking the bounced email notification, which can be found directly in your inbox.

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

## Potential sender bounces

Sender-related bounces occur when issues on your end prevent your emails from reaching recipients. These can include:

- **Poor Sending Reputation**: Your domain or IP address may have been flagged for spammy behavior.

- **Authentication Issues**: Misconfigured SPF, DKIM, or DMARC records can cause your emails to be rejected.

- **High Volume or Speed**: Sending too many emails too quickly can trigger rate limits or blacklisting.

- **550 5.1.8 Access denied, bad outbound sender**
This indicates that Microsoft is flagging the inbox's sending habits, temporarily blocking the email account. 

This issue isn't caused by QuickMail but rather by Microsoft’s actions. 
It’s also not due to invalid email addresses among your prospects.

This can occur if the inbox sends too many emails with identical content, has a low sender reputation, or appears spammy.

Microsoft’s algorithm may flag accounts it suspects of being hacked, compromised, or sending spam. 
To resolve this, please reach out to Microsoft Support to request an unblock.

If you have admin access or an IT admin, you can follow this guide to Restore restricted users in Defender for Office 365

Once the inbox is unblocked by Microsoft, remember to unpause it in QuickMail. 
We automatically pause the inbox if we detect sender-related bounces to prevent further issues.

To solve it, please revisit your cold email strategy to avoid bounces from happening again.

For detailed fixes on these issues, refer to our Fixing Bounces Guide.

-https://help.quickmail.com/deliverability/troubleshooting-handling-sender-related-bounces/

## My leads opened and clicked but they're marked as invalid

Spam filters or opening the sent emails on the inbox can lead to false opens and clicks.
Not to worry because we don't count the bounces on the stats so false opens and clicks won't skew your stats.

## My lead opened, clicked, replied but they still got marked as invalid

The validity of an email is not forever.
People come and go in companies so a lead can be valid today but invalid tomorrow.

Additionally, bounces can also be caused by sender.
It's best to look at the bounce notification to diagnose what happened.
