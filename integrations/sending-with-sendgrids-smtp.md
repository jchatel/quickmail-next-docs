# Sending with SendGrid's SMTP

Using a custom SMTP like SendGrid with QuickMail lets you send emails without relying on your email account’s default sending service. This means you can send a higher volume of emails while reducing the risk of being flagged by your email provider.

**Important:** Using Custom SMTP has Pros and Cons. If you'd like to know more, check out this guide: Should I use Custom SMTP?

## How to use QuickMail with SendGrid's SMTP?

**Step 1** . Log in to your SendGrid account → Dashboard → Create sender identity

![screenshot](../images/000_file-D885LdGPDW.png)

**Step 2.** Fill in the details needed to create a sender

![screenshot](../images/001_file-1uB49F7Z97.png)

**Step 3.** After creating a sender, check your inbox for an email from **no-reply@sendgrid.com** and verify the single sender through that email.

![screenshot](../images/002_file-Q6hyIPJuEq.png)

Here's what the email looks like:

![screenshot](../images/003_file-EoNifDNqKA.png)

You'll be directed to this page in SendGrid once verified.

![screenshot](../images/004_file-09KKpfVoLs.png)

**Step 4.** Once sender is verified, go to SendGrid → Email API → click Integration Guide → choose SMTP relay.

![screenshot](../images/005_file-HuCMv9ENYs.png)

**Step 5** . Next, generate the API key by adding the API Key Name → Create Key

![screenshot](../images/006_file-X9pOSsgrOo.png)

This is how it should look after generating the API key.

![screenshot](../images/007_file-wMFBumordl.png)

**Step 6.** Copy the SMTP configuration from SendGrid

![screenshot](../images/008_file-iahsXv4oPD.png)

**Step 7.** Go to your QuickMail account → Channels → Emails → Click on the email account where you'd like to use SendGrid's SMTP → Sending tab → Fill in the SMTP details → Test Sending

![screenshot](../images/009_file-AfinTa9eVj.png)

**Step 8.** If the configuration is correct in QuickMail, click I've updated my settings and Verify Integration in SendGrid.

![screenshot](../images/010_file-CecUiAmsvv.png)

**Step 9.** Click 'Verify Integration' to send a test email

![screenshot](../images/011_file-MU2H4Kfdvt.png)

If the test email worked, you'll see a message saying it worked.

![screenshot](../images/012_file-RGAXlwJBdz.png)

## Forwarding Bounced Emails from SendGrid

By default, SendGrid does not send bounce reports to the sender's inbox. This means follow-ups may still be sent to bounced leads in QuickMail, which isn't ideal as repeated bounces can negatively affect your sender reputation.

To prevent this, bounce forwarding must be set up in SendGrid so QuickMail can detect bounces and stop follow-ups to those prospects:

While logged in to the SendGrid account, go to Settings → Mail Settings → Forward Bounce Messages

![screenshot](../images/013_file-TLECEkDnce.png)

Select 'Use the From address of the outgoing email' or 'Specify email address' if you'd like to send the bounced emails to a different email → Toglle 'Enabled' → Save

![screenshot](../images/014_file-GQUKEzkxSe.png)

## White-labeling your domain

Authenticating the emails sent out from SendGrid will help with email deliverability.

Setting up SPF and DKIM records in the domain's control panel will improve email deliverability and will remove the "via SendGrid" text in the emails sent out from SendGrid's SMTP.

More information on how to set up SPF and DKIM records here: [https://sendgrid.com/docs/ui/account-and-settings/how-to-set-up-domain-authentication/](https://sendgrid.com/docs/ui/account-and-settings/how-to-set-up-domain-authentication/)
