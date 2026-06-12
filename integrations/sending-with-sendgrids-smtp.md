# Sending with SendGrid's SMTP

Using a custom SMTP like SendGrid with QuickMail lets you send emails without relying on your email account's default sending service. This allows you to send a higher volume of emails while reducing the risk of being flagged by your email provider.

**Important:** Using a custom SMTP has pros and cons. To learn more, check out this guide: Should I use Custom SMTP?

**In this article:**

- How to use QuickMail with SendGrid's SMTP?

- Forwarding bounced emails from SendGrid

- White-labeling your domain

## How to Use QuickMail with SendGrid's SMTP?

**Step 1.** Log in to your SendGrid account → **Dashboard** → **Create Sender Identity**.

![screenshot](../images/000_file-D885LdGPDW.png)

**Step 2.** Fill in the details needed to create a sender.

![screenshot](../images/001_file-1uB49F7Z97.png)

**Step 3.** After creating a sender, check your inbox for an email from **no-reply@sendgrid.com** and verify the sender through that email.

![screenshot](../images/002_file-Q6hyIPJuEq.png)

Here is what the email looks like:

![screenshot](../images/003_file-EoNifDNqKA.png)

You will be directed to this page in SendGrid once verified:

![screenshot](../images/004_file-09KKpfVoLs.png)

**Step 4.** Go to **SendGrid** → **Email API** → **Integration Guide** → select **SMTP Relay**.

![screenshot](../images/005_file-HuCMv9ENYs.png)

**Step 5.** Generate the API key by entering the API key name → click **Create Key**.

![screenshot](../images/006_file-X9pOSsgrOo.png)

Here is what it should look like after generating the API key:

![screenshot](../images/007_file-wMFBumordl.png)

**Step 6.** Copy the SMTP configuration from SendGrid.

![screenshot](../images/008_file-iahsXv4oPD.png)

**Step 7.** Go to **Channels** → **Emails** → click on the email account where you would like to use SendGrid's SMTP → **Sending** tab → fill in the SMTP details → click **Test Sending**.

![screenshot](../images/009_file-AfinTa9eVj.png)

**Step 8.** If the configuration is correct, click **I've updated my settings** in QuickMail, then click **Verify Integration** in SendGrid.

![screenshot](../images/010_file-CecUiAmsvv.png)

**Step 9.** Click **Verify Integration** to send a test email.

![screenshot](../images/011_file-MU2H4Kfdvt.png)

If the test email was successful, you will see a confirmation message.

![screenshot](../images/012_file-RGAXlwJBdz.png)

## Forwarding Bounced Emails from SendGrid

By default, SendGrid does not send bounce reports to the sender's inbox. This means follow-ups may still be sent to bounced leads in QuickMail, which can negatively affect your sender reputation.

To prevent this, set up bounce forwarding in SendGrid so QuickMail can detect bounces and stop follow-ups to those leads.

While logged in to your SendGrid account, go to **Settings** → **Mail Settings** → **Forward Bounce Messages**.

![screenshot](../images/013_file-TLECEkDnce.png)

Select **Use the From address of the outgoing email**, or select **Specify email address** if you would like to send bounced emails to a different address → toggle **Enabled** → **Save**.

![screenshot](../images/014_file-GQUKEzkxSe.png)

## White-Labeling Your Domain

Authenticating emails sent from SendGrid helps improve deliverability. Setting up SPF and DKIM records in your domain's control panel will improve deliverability and remove the "via SendGrid" label from outgoing emails.

For instructions on setting up SPF and DKIM records, see: [https://sendgrid.com/docs/ui/account-and-settings/how-to-set-up-domain-authentication/](https://sendgrid.com/docs/ui/account-and-settings/how-to-set-up-domain-authentication/)
