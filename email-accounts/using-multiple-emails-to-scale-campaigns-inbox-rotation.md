# Using Multiple Emails to Scale Campaigns (Inbox Rotation)

**In this article:**

- Why rotate emails?

- How does it work?

- How to set it up?

- Match the lead's email provider

- How to remove an email from a campaign if its deliverability goes bad?

- I unassigned an email from a campaign but it is still sending emails — why?

- I assigned more emails to a campaign but they are not sending emails — why?

## Why Rotate Emails?

Email rotation allows you to increase the volume of emails sent from a campaign by spreading the load across multiple email accounts. It is also useful when a single campaign needs to be sent by multiple team members.

## How Does It Work?

When a lead starts a campaign, QuickMail randomly assigns them to one of the email accounts assigned to that campaign. All follow-up emails for that lead will then be sent from the same email account for consistency.

**Note:** There is no option to control which leads are assigned to which email account or to set a specific number of leads per email account.

## How to Set It Up?

Go to the campaign → **Channels** tab → under **Emails**, toggle on the email accounts you want to send from.

![screenshot](../images/000_file-0yMo9mCcHv.png)

**Note:** For a detailed guide on adding an email account for sending, check out: Adding an Email Account for Sending.

## Match the Lead's Email Provider

To further improve deliverability, you can enable the option to match each lead's email provider.

When enabled, QuickMail identifies the lead's email provider and assigns them to an email account that uses the same provider. For example, if a lead uses Google, they will be assigned to a Google email account if one is available. The same applies for Microsoft.

If provider matching is not possible, the lead will be assigned to a different email account in the campaign automatically.

### How to Enable It?

Go to the campaign → click the menu icon (three vertical dots) → **Settings**.

![screenshot](../images/001_file-XeoPVkOzCW.png)

Go to the **Advanced** tab → enable **Match Prospect Email Provider**.

![screenshot](../images/002_file-HwwzPKrqhK.png)

## How to Remove an Email from a Campaign if Its Deliverability Goes Bad?

Toggle the email account off from the **Channels** tab in the campaign, the same place where it was assigned.

**Pro tip:** To automate this process, Deliverability AI allows you to group email accounts and automatically swap underperforming ones out of campaigns while putting them into recovery. **Learn more about it here.**

## I Unassigned an Email from a Campaign but It Is Still Sending Emails — Why?

When a lead starts a campaign, QuickMail assigns them to a specific email account and all follow-up emails for that lead continue to be sent from the same email account. Unassigning an email account from a campaign does not reassign leads that are already tied to it.

To reassign those leads to different email accounts:

1. Pause the campaign.

2. Remove the old email accounts from the campaign.

3. Set the campaign live again.

Once the campaign resumes, leads tied to the removed email accounts will be automatically redistributed to the remaining active email accounts.

**Note:** Any other campaigns using the same email account will also need to be paused before it can be removed.

After reassignment is complete, the old email accounts can be added back to the campaign if needed.

If removing the email account is not an option, you can pause it instead to stop emails from being sent. Note that this will delay sending for all leads currently assigned to that email account.

## I Assigned More Emails to a Campaign but They Are Not Sending Emails — Why?

This is the same behavior described above. When a lead starts a campaign, they are assigned to a specific email account and remain tied to it. Adding new email accounts to the campaign does not automatically reassign existing leads to them.

New leads added to the campaign after the additional email accounts are assigned will be distributed across all active email accounts. Existing leads will continue sending from their originally assigned email account.
