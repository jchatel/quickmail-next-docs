# Send Times & Triggers  Demo

**
**

## What are Send Times and Triggers?

To automate campaigns in QuickMail, you need to set up 2 things: Triggers **and **Send times**

- **Send times **dictate when the campaign can send emails.

- **Triggers** allow you to control when and how many leads will start the campaign, but they don't control the email volume.

**

Here's a quick video demo of how to set up this automation:

Note:** It's important to make sure the time zone set for the campaign is correct as you create these automations.

For a complete overview in setting up Send Times and Triggers, check out these guides:

- Optimizing Send Times

- Automate Starting Leads with Triggers

**

## FAQs:

### I don't understand what Triggers are for, what do they do?

When leads are added to a campaign, they will be in a "Not Started" status, and emails won't be sent until some leads start the campaign. You can start leads manually to start sending emails right away or schedule Triggers so leads will start at certain times.

### Do Triggers control email volume?

Not necessarily especially if you have follow up emails. However, it does allow you to control the number of initial emails that will start the campaign daily but not the total volume. If you'd like to set the daily sending limit, check out thisguide.

### Why is my campaign not sending emails even though I've already set up triggers?

When setting up triggers, they cannot be retroactive. For example, if you schedule triggers to start new leads at 8 AM daily and it's currently 12 PM, new leads won't start until the next scheduled trigger, which will be tomorrow.

Additionally, make sure to allow at least 15 minutes when creating or editing Triggers, as the system may sometimes take time to detect changes. For example, if you'd like to start new leads at 8 AM, ensure you set up triggers at least 15 minutes before that time.

###

### How may leads should I add to the Triggers?

The number of leads in the triggers will be equally divided and assigned to the email accounts associated with the campaign. Leads are assigned to the email accounts so that follow-up emails will be sent from the same account.

Use [this calculator](https://docs.google.com/spreadsheets/d/1YmM0d3M6nlBLRcNcT_hCRf8Gatfnj8XTXYL9ZyZ5vUU/edit?gid=0#gid=0) to see the suggested number of leads based on your campaign setup.

### Why can't I add more than 1,000 leads in the Triggers?

Starting 1,000 leads at once may cause a spike in email volume, which can get the email accounts flagged for spamming. If you need to add more than 1,000 leads, it's best to create multiple triggers throughout the day. For example, set 500 leads at 8 AM, 500 at 10 AM, another 500 at 12 PM, and so on

### Why can't I just start all leads immediately?

Starting leads immediately can:

- Lead to a sudden spike in the email volume

- Block the send queue, preventing you from running multiple campaigns at once

- Block the send queue, preventing your follow-ups from sending on time

In QuickMail, emails are sent on a first-come-first-go basis.

This means that whichever email goes into the send queue, will be the first email to send out.

If you start 100 leads in a campaign and you only have 10 daily email limit, your campaign will wait for 10 days before it sends follow-ups. If you want to run another campaign, the same thing could happen and it can even be longer once your follow-ups start sending.

We don't auto-calculate the distribution of initial and follow-up emails yet.

That's why we highly recommend using triggers if you have a large volume of leads.

Can I schedule a specific date when the campaign will start?**

It's not possible to schedule the first trigger for a specific date and time.

Triggers work by checking your campaign schedule and looking for the next available trigger window. Once that trigger runs, QuickMail will start leads automatically, as long as there’s enough daily sending capacity available in your inboxes.

For example, if your trigger is set to run every weekday at 9 AM, any eligible leads will start at the next 9 AM trigger window.

If your inboxes still have available sending capacity for the day, the emails will begin sending immediately during the allowed Send Times.

So while you can control the trigger schedule and sending windows, you can’t set an exact future date for a lead’s very first email to go out.
