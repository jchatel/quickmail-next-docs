# Adding BCC and CC to Emails

**In this article:**

- What is it for?

- How to set up a BCC email?

  - Workspace level

  - Email account level

## What Is It For?

**BCC (blind carbon copy)** allows you to send copies of all outgoing emails in QuickMail to another address. This is commonly used to log emails in a CRM such as Salesforce or HubSpot.

**Warning:** Setting an address that is already added as an email account in QuickMail as a BCC will cause sent emails to be detected as campaign replies, which can mark all journeys as replied.

**CC (carbon copy)** allows you to visibly copy another person on your outgoing emails. Unlike BCC, the recipient can see who has been CC'd. This is useful when you want to:
- Loop in a colleague so they can follow the conversation (e.g., an account executive or manager)
- Copy a shared team inbox for visibility
- Include a partner or consultant who is involved in the outreach

## How to Set Up a BCC Email?

### Workspace Level

Setting a BCC email at the workspace level ensures it is included in every campaign, eliminating the need to apply it to each email account individually.

Go to **Settings** → **General** → under **BCC Email**, fill in the BCC Email field.

![screenshot](../images/000_file-9yNUix4Ye1.png)

### Email Account Level

Setting a BCC email at the email account level adds the BCC address to all emails sent from that specific account. If the workspace has multiple email accounts, only the one with the BCC setting will include the BCC address.

Go to **Email** → click the email account → under **Sending Settings**, fill in the BCC Email field.

## How to Set Up a CC email?
In campaign steps, there are CC fields where you can add an email.
If you want each field to be different for each lead, create a custom property specific for CC > assign emails to them > insert the custom property attribute on the CC field.

FYI: CC and BCC fields are not going to show up on the outbox page.
