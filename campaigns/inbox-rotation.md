# Using Multiple Emails to Scale Campaigns (Inbox Rotation)

**In this article:**
- Why rotate emails?
- How does it work?
- How to set it up?
- Match the lead's email provider
- How to remove the email from a campaign if its deliverability goes bad?
- How to see number of emails sent per email account? 

# Why rotate emails?

Email rotation is set up to increase the number of emails being sent from a campaign.
This is because the volume of emails coming from a campaign will be spread out to the emails assigned to it.
Emails are also rotated if a single campaign must be sent by multiple team members.

# How does it work?

When a lead starts the campaign, QuickMail will randomly choose which email the journey will be assigned. 

The email that sends the initial email will be the same email that will send all the follow-up emails in the campaign.

Note: There's no option yet to set how many leads or which leads will be assigned to which emails.

# How to set it up?

If multiple emails are already added to the account, just go to the campaign channels. Under emails, toggle on emails that you want to send the campaign from.

<img width="1172" height="696" alt="image" src="https://github.com/user-attachments/assets/e3943fcd-72fc-43ee-a04a-b9ecc3cd03a1" />

**Note:** For a detailed guide on how to add an email for sending: https://help.quickmail.com/email-accounts/adding-email-accounts-for-sending/

# Match the lead's email provider

To further improve deliverability you can enable the option to match the lead's email provider.

This feature will identify the email provider for the leads and will match it if possible using the email accounts assigned to the campaign.

For example if the lead has their email service hosted in Google and you assign a Google email account to send from the campaign, that matching email account will be used to send. The same applies for Microsoft as a provider.'

In cases where provider matching isn't possible, the journey will be automatically assigned to a different campaign inbox.

How to set it up?The setting is enabled for each campaign. Go to Campaigns -> Open the campaign -> Options -> Settings. 

Then go to Advanced settings -> Match prospect email provider

# How to remove the email from a campaign if its deliverability goes bad?

You can manually toggle the email off from the same page where you assigned the email.

**Pro tip:**  If you want to do it automatically, we have a Deliverability AI that allows you to group emails and automatically swap the campaign to use the good emails and put bad emails in recovery. 
Learn more about it here.

# I already unassigned the email account from the campaigns but it's still sending emails?

When a lead enters a campaign, QuickMail assigns the lead to a specific **email account**. All follow-up emails for that lead will continue to be sent from the same email account throughout the campaign.

This means that if some leads originally started the campaign from an **unassigned email account**, their follow-up emails will remain tied to that email account unless the assignment is reset.

### How to reassign the leads to different email accounts

To reset the email account assignment:

1. **Pause the campaign.**
2. **Delete the old email accounts** that you want to reassign.
3. **Add or assign the new email accounts** you want to use.
4. **Set the campaign live again.**

Once the campaign resumes, leads that were assigned to the deleted email accounts will automatically be redistributed among the remaining active email accounts when they move to the next email step.

If you plan to use the old email accounts again in the future, you can simply **add them back** to the workspace after the reassignment is complete.

### Important: Other campaigns using the same email accounts

If the old email accounts are currently being used by other campaigns, those campaigns must also be **paused before you delete the email accounts**.

Once the reassignment is complete, you can add the old email accounts back and use them in your campaigns again if needed.

### Alternative: Pause the email accounts

If deleting the email accounts isn't an option, you can **pause the email accounts** to prevent them from sending emails.

However, keep in mind that leads assigned to paused email accounts can't be re-assigned and may be **delayed** in the sequence. 

# How to see number of emails sent per email account? 

To see the number of emails sent per email account, go to the Outbox page and use filter. You can filter messages sent by type, by email account, by channel, and by custom range/date. 

**Note:** The Outbox page stores only the number of emails and LinkedIn messages sent in the past 30 days.
