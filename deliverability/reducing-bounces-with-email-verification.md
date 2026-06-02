# Reducing Bounces with Email Verification

**In this article:**

- What is email verification used for?

- What are the types of email verification status?

- How to configure email verification provider?

- Option 1: QuickMail Verification Credits

- Option 2: External Verification Provider

- How to verify leads?

- Step #1: Enable email verification in the campaign

- Step #2: Add leads to the campaign

- How to know if emails were already verified?

- Troubleshooting: Leads were already added before email verification was setup

# What is Email Verification used for?

Verifying leads in QuickMail is essential to reduce bounce rates and protect sender reputation. QuickMail offers in-app lead verification through email verification credits or integration with third-party providers.

In case you already have an email verification set up with another service, QuickMail also integrates with the following:

- [BriteVerify](https://www.briteverify.com/)

- [DropContact](https://en.dropcontact.io/)

- [Hunter](https://hunter.io/email-verifier)

- [NeverBounce](https://neverbounce.com/)

- [ZeroBounce](https://www.zerobounce.net/)

- [Bouncer](https://www.usebouncer.com/)

# What are the types of Email Verification status?

There are 5 types of email verification status:

- Not Verified – Emails that have not yet been verified or whose verification status has expired.
Emails that are not verified yet are displayed in black.

- Invalid – An invalid email address is one that has been verified as a bad recipient address (e.g., it does not exist or is not accepting mail).
Emails that are invalid are displayed in red.

- Valid – A valid email address is one that is safe to send emails to.
Emails marked as valid are displayed in green.

- Unknown – These are email addresses for which we could not receive a response. This might be due to server issues or other problems that prevented successful verification.
Emails marked as unknown are displayed in gray.

- Risky – Risky emails include those from "Accept All" domains (which might later reject your email), "Unknown" domains (which are unresponsive), "Role-Based" addresses (like sales@ or support@, typically managed by multiple people and prone to complaints), and "Temporary" addresses (which are only valid for a short time). Emails marked as risky are displayed in orange.

# How to Configure Email Verification Provider?

To setup email verification, QuickMail verification credits must be purchased or a third-party email verification provider must be integrated first. After purchasing email verification credits, proceed to How to Verify Leads?

## Option 1: QuickMail Verification Credits

For single workspaces:** To purchase email verification, go to Settings -> integrations -> buy email QuickMail credits.

![screenshot](../images/000_file-lZjNkyGGyS.png)

**For Agencies: **Users can purchase Email Verification credits in the agency dashboard settings

![screenshot](../images/001_file-eEWwDlPz0P.png)

**Note:** It costs $10 per 1,000 QuickMail verification credits. It's billed one-time

Once email verification credits are purchased, the number of available credits will show up under Settings → Integrations →  Email Verification

![screenshot](../images/002_file-l0HeAoOfmD.png)

## Option 2: External Verification Provider

In case you already have an email verification set up with another service, QuickMail also integrates with the following:

- [BriteVerify](https://www.briteverify.com/)

- [DropContact](https://en.dropcontact.io/)

- [Hunter](https://hunter.io/email-verifier)

- [NeverBounce](https://neverbounce.com/)

- [ZeroBounce](https://www.zerobounce.net/)

- [Bouncer](https://www.usebouncer.com/)

Once you have an account with one of the external services above, head to the Settings → Integrations → Click on Configure External Provider

![screenshot](../images/003_file-ERQeHjgUTG.png)

After that, select your preferred External Email Verification Provider and enter the API key from the external email verification provider.

![screenshot](../images/004_file-JI1wBTL591.png)

Once the external email verification provider has been setup, it will show the available email verification credits from that provider.

![screenshot](../images/005_file-30UmZoYLST.png)

# How to Verify Leads?

## Step #1: Enable Email Verification in the Campaign

Once an email verification provider has been setup, go to your preferred campaign → Click on the three vertical dots at the upper right hand corner → Settings →Adding leads tab →  Toggle Verify Emails →  Select Email Verification Provider

![screenshot](../images/006_file-lni7VBCS4V.png)

Depending on your preference, it's possible to set the campaign to reject invalid, risky, or emails with unknown validity

![screenshot](../images/007_file-TznH8GO6UX.png)

## Step #2: Add Leads to the Campaign

Once email verification settings are enabled in the campaign, they will serve as a filter and automatically verify leads when they are added to the campaign.

There are two ways to add leads to the campaign:

- ### Add leads to the campaign manually

To add leads to the campaign manually, simply head to List → Select leads → Add to campaign (+ sign icon)

![screenshot](../images/008_file-PAjLCy3QEX.png)

- ### Add leads via import

To add leads via import, go to List → + Leads → Import from CSV or Google Drive → Select Drive or CSV

![screenshot](../images/009_file-qA36pilQNG.png)

After selecting a Drive or CSV, make sure to select a column for the email address of the lead.

![screenshot](../images/010_file-ebvl8rHE1e.png)

Then, go to Options → Select the Campaign where you would like to add the leads → Check the box "Update lead if it exists"

![screenshot](../images/011_file-MvjhnmMY1s.png)

If leads are invalid, risky, or have unknown validity, they will still be adding to the account. However, depending on the campaign's verification settings, some leads will be rejected from being added to the campaign.

# How to know if leads have already been verified?

To see if emails have been verified, we will need to filter them based on their email verification status.

To do that, go to List → Filters → Email verification: Not Verified, Invalid, Valid, Unknown Validity, Risky

![screenshot](../images/012_file-XkfJSyeH6S.png)

**Note:** Leads that have already been verified won't use email verification credits again

# Troubleshooting: Leads were already added to the campaign before email verification was setup

Enabling email verification in the campaign after the leads have already been added won't verify the existing leads in the campaign.

Therefore, leads that have not yet started must be removed and re-added to the campaign.

On the other hand, leads that have already been sent an email will be automatically verified by the system as either valid or invalid.

To remove and re-add leads that have not yet been verified, go to List → Filters → Under Email verification, select Not Verified

![screenshot](../images/013_file-JWXfOoev8D.png)

We need to narrow down the filtered list by campaign so to do that, add another filter by going to the campaigns tab → select a campaign under "Has started any of the following campaign"

![screenshot](../images/014_file-yno4A30DYf.png)

After filtering the leads, select all leads → Cancel campaign → Confirm

![screenshot](../images/015_file-AqXx143iWo.png)

After canceling the leads, go to the campaign where they're in → Leads → Filters → Canceled

![screenshot](../images/016_file-9LksYrCZ4T.png)

After canceling the leads, select all leads → Export them (CSV will be sent to the email address you're using to login) → Once export is received, Delete

![screenshot](../images/017_file-eexzjGgxmg.png)

After deleting the leads from the campaign, double check if email verification is setup in the campaign.

![screenshot](../images/018_file-q0lRz556SY.png)

When reimporting the CSV, make sure to select the campaign where you would like to add the leads and check the box "Update prospect if it exist". Otherwise, the import will be rejected and the leads won't be re-added.

![screenshot](../images/019_file-uLAaP8qfNK.png)

## There are invalid leads added to my campaign, what should I do?

Leads marked as invalid will not be contacted. Instead, they will run into an error to prevent bounces.

You can keep them in the campaign but it might be worth removing them to avoid confusion.
