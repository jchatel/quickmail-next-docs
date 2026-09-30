# Company Colleagues Attribute

## In this article:

- What is company colleagues attribute?
- How does it work?
- Things to keep in mind
- How to use it in an email? 
- How to CC colleagues in emails? 
- Why am I getting an error?

## What is company colleagues attribute?

```{{=company.colleagues}}``` is a precomputed attribute that automatically fills in the names of a lead's colleagues, meaning other leads from the same company or domain. 
When the email is sent, QuickMail replaces the attribute with each colleague's name, or their email address if no name is available.

This is useful when you reach out to several people at the same company and want each person to know who else you contacted.

## How does it work?

QuickMail groups leads into companies based on their company name or email domain. Leads in the same company are treated as colleagues.

> **IMPORTANT:** If a company is not mapped during import, QuickMail will automatically assign a company based on the leads' domains.

For example, say these three leads are in your workspace:

| Lead | Email | Company |
| --- | --- | --- |
| Richard Hendricks | richard@piedpiper.com | Pied Piper |
| Monica Hall | monica@piedpiper.com | Pied Piper |
| Jared Dunn | jared@piedpiper.com | Pied Piper |

Since all three share the `piedpiper.com` domain, they are grouped under the company **Pied Piper** and are colleagues of each other.

Now, add the attribute to an email step in the email editor:

```
Hi {{lead.first_name}},

I also reached out to {{=company.colleagues}} since you all work on the product team at {{company.name}}.
```

When the email is sent to Richard, QuickMail replaces `{{=company.colleagues}}` with the names of his colleagues. Richard's own name is left out, since he is the one receiving the email:

```
Hi Richard,

I also reached out to Monica Hall and Jared Dunn since you all work on the product team at Pied Piper.
```

The same thing happens for each lead. Monica's email would mention Richard and Jared, and Jared's email would mention Richard Hendricks and Monica Hall.

## Things to keep in mind

- **For leads whose colleagues don't have a name.** QuickMail will automatically use the colleague's email address.
- **Only use this attribute for leads who have colleagues.** Sending an email with `{{=company.colleagues}}` to a lead who doesn't have a colleague will cause the lead to run into an error in the campaign.
- **Be careful when sending to free email domains like gmail.com, hotmail.com, etc.** Leads who share the same free domain may be treated as colleagues, so unrelated people might be mentioned incorrectly.
- **Colleagues are matched by company or domain.** Make sure your leads' company names are correct and written exactly the same way, since even small differences in spelling can stop them from being matched.
- **Test before launching.** Send a test email to check how the colleague. Here's a guide: (Sending Test Emails)[https://help.quickmail.com/campaigns/sending-test-emails/]

## How to use it in an email?

Add the attribute ```{{=company.colleagues}}``` to the body of any email step, or go to the email step → { } → Formula → Colleagues

<img width="850" height="532" alt="image" src="https://github.com/user-attachments/assets/cb7fb7de-45be-4176-b992-2cff65a1a6f4" />

## How to CC colleagues?

You can also add `{{=company.colleagues}}` to the **CC** field of an email step **only if the leads don't have a name**. This copies the lead's colleagues from the same company on the email.

> **Tip:** If two or more leads from the same company are in the same campaign, each lead will receive their own email, and their colleagues will be CC'd on each one. This means the same people may receive several copies of similar emails._

<img width="898" height="558" alt="image" src="https://github.com/user-attachments/assets/0e0c00db-a922-459f-ae4b-87a806dd7abb" />

## Why am I getting an error?

The colleagues attribute always needs a value to fill in. If it can't find the right value, QuickMail stops the email instead of sending it with a broken or empty placeholder. This can happen in two places:

### In the email body

If a lead has **no colleagues** in QuickMail (no other leads with the same company or email domain), there is nothing to fill in.

When this happens, the email will not be sent, and the lead's journey will stop with an error.

**To fix it:** Remove the lead from the campaign, or move them to a campaign that doesn't use `{{=company.colleagues}}`.

### In the CC field

The CC field needs **email addresses** to work. However, when colleagues have a name saved in QuickMail, `{{=company.colleagues}}` fills in their **names** instead of their email addresses. Since a name can't be used to CC someone, the email can't be sent and will result in an error. 

**To fix it:** Create a custom field that stores the colleagues' email addresses, then add that custom field to the CC field instead of `{{=company.colleagues}}`.

1. Create a custom field, for example `Colleague_Emails`.
2. For each lead, add their colleagues' email addresses to this field, **separated by commas**:

```
   monica@piedpiper.com, jared@piedpiper.com
```

3. Add `{{lead.custom.Colleague_Emails}}` to the **CC** field of the email step.

> **Tip:** If you import the email addresses using a CSV file, wrap the value in **quotation marks**, since commas are normally used to separate columns in a CSV:
>
> ```
> email,Colleague_Emails
> richard@piedpiper.com,"monica@piedpiper.com, jared@piedpiper.com"
