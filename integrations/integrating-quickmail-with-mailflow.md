
# Integrating QuickMail with Mailflow

**Note:** You need to create an account in [MailFlow](https://www.mailflow.io/) to use the integration with QuickMail. If you don't have an account set up yet, please check out this [Quick Setup Guide](https://help.mailflow.io/article/428-getting-started).

Our QuickMail integration allows users to automatically sync their inbox deliverability scores from Mailflow to QuickMail. The inbox deliverability scores are based on the auto-warmer emails sent from Mailflow. 
With this, users won't have to frequently login to Mailflow to monitor the deliverability scores of their inboxes.

## How does the integration work? 

It's automatic! Simply add the same inbox to both Mailflow and QuickMail. Once the inbox starts sending auto-warmer emails, the inboxes in QuickMail will be scored accordingly.
Note that if the inbox isn't in QuickMail, the inbox score will only show up in Mailflow.

If you need help with adding inboxes in Mailflow & QuickMail, check out these guides:
* [QuickMail - How to add an inbox for sending email campaigns?](https://help.quickmail.com/email-accounts/adding-email-accounts-for-sending/)
* [MailFlow - How to add a Google inbox?](https://help.mailflow.io/article/410-adding-google-inboxes)
* [MailFlow - How to add a Microsoft inbox?](https://help.mailflow.io/article/411-adding-outlook-inboxes)
* [MailFlow - How to add a Custom inbox?](https://help.mailflow.io/article/412-adding-custom-inboxes)

## Why is the inbox not showing any scores? 

An inbox cannot be scored if it's not sending auto-warmer emails in Mailflow. Here are several reasons why the inbox isn't sending auto-warmer emails:

The inbox hasn't started sending auto-warmer emailsThe inbox must be added to the auto-warmer group to enable Auto-Warmer. Otherwise, the inbox won't start sending auto-warmer emails. 
It may take up to 48 hours before the inbox starts sending auto-warmer emails. So you may not see auto-warmer emails being sent from the inbox immediately.

If you need help with adding the inbox to the auto-warmer group, check out this guide: [Auto-Warmer](https://help.mailflow.io/article/414-how-to-use-the-auto-warmer-feature)
If the inbox wasn't accepted to the auto-warmer group, check out this guide: [Troubleshooting Errors](https://help.mailflow.io/article/497-why-cant-i-join-the-auto-warmer-group)

The inbox stopped sending auto-warmer emails because we lost access to the inboxWe may lose access to the inbox due to changes in the email account's settings, a security check by the email provider, or if app access was revoked. So to continue sending auto-warmer emails, the inbox must be reauthenticated.

If you need help with reauthenticating an inbox in Mailflow, here's a guide that might come in handy: [Reauthenticating Inboxes](https://help.mailflow.io/article/422-how-to-re-authenticate-google-inboxes)
