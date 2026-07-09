# Troubleshooting: Common Lead Errors

## Why did my lead run into an error?

A lead can run into an error in a campaign for a variety of reasons. This article explains the most common error messages you may encounter, what they mean, and the steps you can take to resolve them.

## Where to find the cause of a lead error?

When a lead runs into an error, its status on the campaign's Leads page will change to _'Error Running'_.

To see why the lead encountered an error, simply hover over the Error Running status. A tooltip will display the reason for the error.

## Common lead errors and how to fix them

### Linked In Related Errors

| Error | What it means | How to fix |
|-------|---------------|------------|
| Campaign has no LinkedIn account to execute this LinkedIn step | The campaign contains a LinkedIn action, but no LinkedIn account is assigned. | Assign a LinkedIn account to the campaign and then resume the lead progress |
| Action temporarily blocked by LinkedIn due to high connection or messaging activity | LinkedIn has temporarily restricted your account because you've reached its activity limits. | Stop sending connection requests or messages and wait for the restriction to expire. Depending on the type of restriction, it may last from a few hours to about a week. Resume activity gradually to avoid being restricted again |
| This profile blocked you on LinkedIn | The lead has blocked your LinkedIn account. | This action cannot be completed. Skip the lead or use another LinkedIn account if appropriate |
| Message cannot be sent. You are not yet connected with this lead on LinkedIn. Send a connection request first. | The workflow attempted to send a regular LinkedIn message before you were connected. | Send a connection request first or use an InMail step instead |
| You do not have enough InMail credits to send this message | Your LinkedIn account has run out of InMail credits. | Wait for your monthly InMail credits to renew or purchase additional credits through LinkedIn |
| Unable to fetch lead's LinkedIn profile information. Please check the LinkedIn profile provided and try again. | The lead's LinkedIn profile could not be accessed. | Verify that the LinkedIn profile URL is correct and that the profile still exists |
| Unable to fetch conversation information | The LinkedIn conversation could not be retrieved. | Refresh or reconnect the LinkedIn account and verify that the conversation still exists |
| The previous LinkedIn connection request was declined or withdrawn. You can try again in a few days. | LinkedIn prevents sending another connection request immediately after one was declined or withdrawn. | Wait a few days before sending another connection request. |
| Cannot send InMail. Your LinkedIn account is not Premium. | InMail requires a LinkedIn Premium subscription. | Upgrade to LinkedIn Premium or replace the step with a regular LinkedIn message after connecting |
| Unable to add connection | The connection request failed for an unspecified reason. | Retry later and verify that the LinkedIn account is connected and not restricted |
| Unable to get profile | The LinkedIn profile could not be loaded. | Verify the LinkedIn profile URL and reconnect the LinkedIn account if needed. |
| Unable to send voice message. This member cannot be messaged because they are not a connection. | Voice messages can only be sent to 1st-degree connections. | Connect with the lead before sending a voice message |
| Cannot send a message while an InMail is awaiting response | LinkedIn only allows one active InMail conversation until the recipient replies. | Wait for the recipient to respond before sending another InMail |
| You can only send one InMail per lead | LinkedIn only allows one InMail to be sent to the same lead. | Do not attempt to send multiple InMails to the same lead |
| Unable to add connection (Fuse limit exceeded) | Your account reached the connection request limit enforced by LinkedIn. | Reduce connection activity and wait until the limit resets before sending more requests |
| Unable to add connection (Custom invite limit reached) | LinkedIn has reached the limit for connection requests that include a personalized note. | Wait until the limit resets or send connection requests without a personalized note. |
| Unable to add connection (Custom message too long) | The personalized invitation exceeds LinkedIn's character limit. | Shorten the personalized invitation message |
| Unable to add connection (Can't resend yet) | LinkedIn does not allow another connection request to this person yet. | Wait until LinkedIn allows another invitation to be sent |
| Unable to send InMail (Fuse limit exceeded) | Your account has reached the InMail sending limit. | Wait until the limit resets and reduce daily InMail activity before sending more InMails |


### Email Related Errors
| Error | What it means | How to fix |
|-------|---------------|------------|
| No variation available for the prospect on this step | The campaign couldn't find an email variation to send to this lead. This usually happens when the variation or step is paused, havebeen deleted, or doesn't match the lead's conditions. | Ensure the step has at least one active email variation that the lead is eligible for |
| Unexpected token at HTML... Forbidden (403) | QuickMail received a **403 Forbidden** response while trying to render the email, typically because an external resource or URL used in the email is inaccessible. | Check any external resources (such as images or hosted content) referenced in the email template and ensure they are publicly accessible |
| Error in message: Could not transform inbox name | QuickMail couldn't replace the **Inbox Name** personalization variable with a value. | Verify the sending inbox is properly configured and that the inbox has a valid display name |
| Error in message: Could not transform inbox signature | QuickMail couldn't insert the sending inbox's signature into the email. | Verify the sending inbox has a signature configured, or remove the inbox signature personalization variable from the template |
| Error in message: Could not transform company name | QuickMail couldn't replace the **Company Name** personalization variable because no value was available. | Ensure the lead has a company name populated, or remove the company name personalization variable from the email template |
| Can't continue journey. The campaign step variation it was on was deleted. | The lead was assigned to a step or variation that has since been deleted from the campaign. | It's no longer possible to fix this due to broken sequence The workaround is to delete and re-add the lead to restart the sequence |
