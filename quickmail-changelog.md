# QuickMail Changelog

## July 21, 2026
### FEATURES
- Lead's Location, Language, and Company name will now be imported too when importing leads from a LinkedIn post. 

## July 15, 2026
### FEATURES
- Added company size as an ICP filter, making it easier to import LinkedIn leads that fit your target audience.

## July 14, 2026

### FIXES
- Some messages were not showing in Opportunities
- LinkedIn campaigns continued sending follow-up messages even after a recipient's reply had been detected.

## July 9, 2026

### FIXES
- Bulk assigning thousands of senders to a campaign was leading to an error
- Adding new LinkedIn accounts via 2FA was leading to an error

## July 5, 2026

### FIXES
- Reversed the order of the campaign lead progress bar
- Removed emojis from LinkedIn imports and fixed auto-capitalization for first and last names

## July 2, 2026

### FEATURES
- Added support for ICP filtering "Open to Work" leads in LinkedIn Profile View and LinkedIn Profile Import
  <img width="1248" height="701" alt="image" src="https://github.com/user-attachments/assets/a43e4b68-00c0-4a79-9e04-d302c614c1a7" />


## June 30, 2026

### FEATURES
- Ability to bulk update email account sender names

  <img width="642" height="503" alt="image" src="https://github.com/user-attachments/assets/de6191aa-185e-4ad5-a665-4c282d875431" />


## June 25, 2026

### FIXES
- New domains purchased from QuickMail were not sending autowarmer emails due to forwarding.

## June 24, 2026

### FEATURES
- When a LinkedIn account is temporarily restricted due to exceeding connection request or messaging limits, the system will automatically pause LinkedIn sending activity and retry after 24 hours. 

## June 17, 2026

### FEATURES
- Email account and LinkedIn account invite links are now valid for 30 days instead of 24 hours. 

## June 15, 2026

### FIXES
- Leads can now only be added to campaigns within the workspace where they were originally created. This prevents errors that could occur when attempting to add a lead to a campaign in a different workspace.

## June 11, 2026

### FEATURES
- LinkedIn Opportunity replies are now processed asynchronously

## June 9, 2026

### FEATURES
- Ability to manually import leads from a LinkedIn post to a QuickMail campaign
<img width="1287" height="701" alt="image" src="https://github.com/user-attachments/assets/bfa7780e-fb01-438d-ae39-adbe75afc66f" />
  

## June 2, 2026

### FEATURES
- Common lead errors related to LinkedIn now include clearer explanations and context
- Deliverability reports are now available in the email account settings
  
<img width="844" height="703" alt="image" src="https://github.com/user-attachments/assets/9b740713-4801-4bd3-ae56-ea93993b4b06" />

## May 27, 2026

### FEATURES

- Guest logins can now access LinkedIn Browser Extension so they can easily add their LinkedIn account to QuickMail

- Ability to buy email verification credits

![screenshot](../images/000_file-l0vajJdbEN.png)


## May 23, 2026

### FEATURES

- Added ICP filters for LinkedIn post and profile viewer imports, allowing only matching LinkedIn profiles to be imported into campaigns.

![screenshot](../images/001_file-fixsuxXetF.png)

### FIXES

- Rolled out improvements to the LinkedIn browser extension to ensure a smoother user experience.


## May 15, 2026

### FEATURES

- Ability to connect LinkedIn accounts via browser extension, for a faster and easier setup

![screenshot](../images/002_file-qzmhsSJLMl.png)

### FIXES

- When sending test emails, the campaign preview didn't show instant LinkedIn follow ups

- Improved LinkedIn account syncing


## May 10, 2026

### FEATURES

- Ability to broadcast emails by simply selecting multiple leads in the main Leads page. This also creates a one-step email campaign, adds the selected leads, and starts sending immediately

![screenshot](../images/003_file-cFlRffXsb1.png)


## May 5, 2026

### FEATURES

- Ability to add LinkedIn accounts via invite link, allowing users to easily connect accounts even without direct access to the LinkedIn credentials for faster onboarding.

![screenshot](../images/004_file-NcV42wBnG0.png)


## May 1, 2026

### FIXES

- Importing leads via Sales Navigator was being allowed in the interface, but it was running into an error when it was not included in the plan

- Auto-warmer emails being forwarded were being shown in the auto-warmer report.


## April 25, 2026

### FEATURES

- New email accounts added to QuickMail’s Auto-warmer pool will now receive 5 autowarmer emails before sending the first autowarmer email, improving email deliverability

### FIXES

- Users were unable to set the campaign live when the campaign name was too long


## April 23, 2026

### FEATURES

- Ability to import leads from LinkedIn Post

![screenshot](../images/005_file-5HgzzgefWi.png)

- Users can now archive and unarchive campaigns for smoother campaign management.

![screenshot](../images/006_file-L0S5lqeLK6.png)

### FIXES

- Fixed delays in sending instant LinkedIn follow-up messages

- Improved domain ordering for better performance and consistency

- Weekly deliverability reports were not sent for accounts with a large number of inboxes

- Optimized auto-warmer content to increase email deliverability performance


## April 8, 2026

### FEATURES

- Conditions are now also cloned when cloning a campaign

- Ability to send instant LinkedIn follow up messages

![screenshot](../images/007_file-8Y2ajwiAOJ.png)

- Ability to add attachments to LinkedIn messages

![screenshot](../images/008_file-JHXDH4GAku.png)

### FIXES

- Triggers were not getting cloned when cloning a campaign

- Opportunities were not infinitely scrolling


## March 31, 2026

### FEATURES

- LinkedIn accounts are now being synced for replies and connection requests every hour for faster communication

### FIXES

- Some LinkedIn replies weren’t being detected. We’ve made reply detection more reliable


## March 20, 2026

### FEATURES

- Ability to import profile viewers automatically

![screenshot](../images/009_file-87GQgyEE37.png)


## March 17, 2026

### FEATURES

- LinkedIn connection requests are automatically withdrawn after 90 days to comply with LinkedIn’s policies. This also provides an opportunity to retarget leads effectively through LinkedIn outreach campaigns

### FIXES

- Lead progress were running into an error when generating a LinkedIn Profile View


## March 5, 2026

### FIXES

- Email notifications were not being sent or were containing missing information

- Logging in via LinkedIn was not working

- Improved performance for bulk deleting leads


## March 3, 2026

### FIXES

- Improved autowarmer content


## March 1, 2026

### FEATURES

- LinkedIn Connection Acceptance Rate on stats per email step and variation

- Ability to filter campaigns by excluded and included workspace via API


## February 26, 2026

### FIXES

- Users were not able to reply to leads with LinkedIn profile IDs that contained special characters


## February 24, 2026

### FEATURES

- Ability to add tags and custom properties via API

- Sample data in Zapier now includes lead's language

### FIXES

- When manually uploading a LinkedIn Voice message, the 'Add' or 'Update' button was disabled

- Optimized system to prevent system latency


## February 5, 2026

### FEATURES

- Users can now send InMails via QuickMail campaigns.

![screenshot](../images/010_file-NfIg5hzsx3.png)

### FIXES

- Fixed an issue where the renewal date showed incorrectly when switching to yearly

- Improved LinkedIn Voice Messaging

- Clarified LinkedIn error messages when leads encountered an issue, making them more informative

- When 'Wait Until Connection Request is Accepted' was disabled, LinkedIn acceptances didn’t create opportunities


## January 28, 2026

### FIXES

- Some users couldn’t send messages or replies on LinkedIn because LinkedIn was deprecating an endpoint.


## January 22, 2026

### FEATURES

- Ability to record and send voice messages to LinkedIn.

![screenshot](../images/011_file-biMUhBKU4Y.png)

### FIXES

- When a lead replied and was added to another campaign, the lead did not start if the campaign used triggers.


## January 8, 2026

### FEATURES

- Option to create or not create an Opportunity when a lead accepts LinkedIn Connection. This allows users to keep their Opportunities page clutter free.

![screenshot](../images/012_file-bw8L2XXg2R.png)


## December 11, 2025

### FEATURES

- Users can now see the acceptance rate of LinkedIn connection requests in the campaign stats.

- Filter for inboxes that are accredited and not accredited in the Channels page.

## December 10, 2025

### FEATURES

- Ability to filter LinkedIn connection stages, allowing users to see whether contacts are 1st, 2nd, or 3rd-degree connections..

## December 4, 2025

### FEATURES

- Opportunity link is now visible in the Lead’s Quick View. This makes it easier for users to access the conversation with the lead, especially when related opportunities are pending or archived, and might otherwise be overlooked.

![screenshot](../images/013_file-Wp1k6VKB8h.png)

### FIXES

- When adding custom domain tracking, it sometimes shows an error stating that the SSL is pending, even though it has already been verified.

## November 28, 2025

### FEATURES

- Users can now add leads to the DNC based on their LinkedIn account ID.

![screenshot](../images/014_file-BDUNunqv5P.png)

- There's now an option to delete Drives and Auto-Imports in the interface.

### FIXES

- The sent email statistics were calculated using GMT+0 timezone instead of the user’s account timezone, which caused confusion.

## November 26, 2025

### FEATURES

- Ability to allow leads to skip a LinkedIn Connection Request, if the lead is already connected.

![screenshot](../images/015_file-R45JCgJtfJ.png)

- LinkedIn account quickview now displays all campaigns the Linkedin account is assigned to, similar to how campaigns are shown for inboxes.

![screenshot](../images/016_file-lmqC4uilyb.png)

### FIXES

- Inbox properties are now supported in LinkedIn Steps. This includes inbox signature, allowing users to set and automatically insert a signature when sending messages through LinkedIn campaigns.

## November 19, 2025

### FIXES

- Autowarmer replies in QuickMail shows the sender's fake company name instead of the receiver's.

## November 7, 2025

### FEATURES

- Users can now view detailed progress steps for each pending domain order in the overview.

### FIXES

- We’ve fixed a bug that caused LinkedIn connection request messages to be missing from Opportunities.

## October 31, 2025

### FEATURES

- Users now have a better overview of pending domain orders

![screenshot](../images/017_file-xERKpqelrC.png)

- Conditions are now available in the new UI, no need to switch back and forth to the old UI.

![screenshot](../images/018_file-iksc36Z7Vx.png)

### FIXES

- If a lead replies to a campaign that is later deleted, any opportunities linked to subsequent campaigns will not be visible.

- Autowarmer emails are now only sent on business hours

- Weird characters showing in the Outbox for sent emails to Outlook recipients

- The campaign was not getting paused when there's no LinkedIn account assigned to a campaign after adding a LinkedIn Step. This was causing leads to run into an error.

- Optimized LinkedIn reply tracking

## October 28, 2025

### FEATURES

- Ability to export Opportunities

![screenshot](../images/019_file-zqQGSwzBDF.png)

### FIXES

- When cloning a campaign, the sharing settings was being defaulted to Private

- Domains with the words "gmail" and "google" weren't allowed when buying a domain in QuickMail

- When a lead blocks a LinkedIn user, the journey previously ran into the error “Unable to fetch profile information.” We’ve added better error handling for this scenario, so the message will now clearly indicate that the lead has blocked the LinkedIn user.

## October 20, 2025

### FIXES

- There were still instances where sender email address isn’t automatically selected when replying to Opportunities.

- Enhanced Opportunities functionality

## October 14, 2025

### FIXES

- There were still some journeys running into an error due to LinkedIn profile error

## October 9, 2025

### FEATURES

- Users can now switch workspaces without having to go to the Agency Dashboard

![screenshot](../images/020_file-ZtjRP698HT.png)

### FIXES

- Sometimes, the sender email address isn’t automatically selected when replying to Opportunities.

- Improved modal for ordering Google domains

## October 6 2025

### FIXES

- Some LinkedIn accounts can't process actions which caused lead progress to run into an error

## September 30, 2025

### FEATURES

- Ability to purchase Reword with AI credits in the Billing/Plan page, so users won’t have to reach out to Support to continue sending emails after running out of AI credits.

- More audit info on the change log

- Attachments can now be added when sending replies from Opportunities

- The *To:* section in Opportunities can now be updated if you’d like to change the initial contact person

![screenshot](../images/021_file-acERej2AaL.png)

### FIXES

- The language in HubSpot wasn’t getting updated after updating it in QuickMail.

- Sales Nav import was starting even though the LinkedIn account was paused, which was causing an error.

## September 23, 2025

### FIXES

- Sales Navigator Autoimport was not enabled by default to Growth and Agency Plans

## September 15, 2025

### FIXES

- Fixed an issue where Journeys encountered errors when using Reword with AI, helping ensure smoother automation.

## September 11, 2025

### FEATURES

- Email accounts purchased through QuickMail can now join the Autowarmer group directly from the interface, making setup faster and easier.

- When a campaign has no leads, the option to upload leads is now more visible in the Leads page, saving time when adding new prospects.

![screenshot](../images/022_file-NiKiso0edr.png)

### FIXES

- Opportunities will no longer get unarchived without a lead’s reply.

- Removed duplicate items in Opportunities for a cleaner view.

- Fixed an issue where Opportunities became inaccessible when there are LinkedIn sent items.

- Opportunities now correctly unsnooze when changed to an active state.

- Fixed cases where LinkedIn accounts occasionally failed to sync for replies.

## September 3, 2025

### FIXES

- LinkedIn replies sent by users were getting duplicated

## September 3, 2025

### FEATURES

- Sent LinkedIn messages will now appear in Opportunities, allowing users to easily follow the conversation thread.

### FIXES

- Saved private campaigns weren't showing up in the campaign library

- LinkedIn replies sent by users were getting duplicated in Opportunities

- Replies to LinkedIn connection request messages were not getting detected

- Replies on same Opportunities were not arranged by the date they were created

## August 27, 2025

### FIXES

- The autowarmer emails didn't include fake company names set

## August 21, 2025

### FEATURES

- Ability to see how many leads are on a specific step in a campaign

![screenshot](../images/023_file-pfNOMHx3L2.png)

- Autowarmer emails are now receiving replies, which makes the warm-up process more effective in improving deliverability

- The account plan wasn't being updated after deleting a domain purchased from us

### FIXES

- Campaign stats weren't calculated in real-time sometimes

- LinkedIn imports were not being recorded in the changelog

## August 14, 2025

### FEATURES

- Ability to add avatars to email accounts purchased from QuickMail

### FIXES

- Changed the text in the cancellation window so users can now see the last day they’ll have access to their account, as well as the exact date when the cancellation takes effect.

- Fixed an issue where the campaign list in the campaign library failed to load properly when there were 30 or more campaigns due to pagination errors.

## August 11, 2025

### FEATURES

- Added a warning when buying emails to indicate that they cannot be modified once purchased

- The Past Invoices tab will now be the default when accessing the Invoices page. This allows users to easily see past invoices

### FIXES

- Expired accounts can't resubscribe due to an error

- Clicking a campaign under the Owner and Name columns didn’t open the campaign

## August 4, 2025

FIXES

- The reply count in the step stats and the total campaign did not match.

- Campaigns with data recorded over several weeks weren’t correctly totaled on the step stats page

- The tooltip to see the complete name of the campaign were not showing.

- The changelog was not showing errors encountered during a plan change.

## July 24, 2025

### FEATURES

- User will now be notified via email after a purchased Google email account is added to their account

### FIXES

- The Sales Navigator import was sometimes not being sent to the user who did the import

## July 17, 2025

### FEATURES

- Ability to mimic recipient names to help boost engagement.

- Sales Navigator import will now cease automatically when the account lead limit is reached.

- Languages being added as one of the default properties of leads.

### FIXES

- Fixed an issue where LinkedIn accounts were getting disconnected when importing from Sales Nav

- Updating the Sales Nav import was causing an error

- The domain availability check was not being updated immediately after purchasing a domain, which could lead to accidentally re-purchasing the same domain or email accounts via the cart

## July 9, 2025

### FEATURES

- You can now right-click on Opportunities and open them in a new tab, just like a regular link.
This helps improves usability and makes multitasking easier.

- Improved LinkedIn Automation to help lessen disconnects

- Ability to cancel subscription when there are active domains purchased from QuickMail. No need to reach out to Support.

## July 1, 2025

### FEATURES

- Auto-import from Sales Navigator

- Ability to clone an email variation step to save users time.

![screenshot](../images/024_file-d6CtIk4I49.png)

## June 26, 2025

### FEATURES

- Ability to import from Sales Navigator

![screenshot](../images/025_file-lELFQVhCYe.png)

- The campaign owner now shows in the campaign list

### FIXES

- Tags and custom attributes were not syncing to Pipedrive

## June 20, 2025

### FEATURES

- Option to filter leads based on whether they have a LinkedIn profile attached.

- Ability to use liquid syntax with LinkedIn messages and connection requests

### FIXES

- Better auto-warmer messages for email exchanges to look more natural

- Domain forwarding verification process fails to differentiate between .co and .com domains at the time of purchase.

###

## June 16, 2025

### FEATURES

- Ability to open campaigns in another tab from the campaign list. This allows users to easily access multiple campaigns without going back and forth the campaign list

### FIXES

- Trial users were able to add more than 100 leads. Limit on trial is only 100 leads

## June 9, 2025

### FEATURES

- Premium Autowarmer for Google inboxes purchased from QuickMail

### FIXES

## May 28, 2025

### FEATURES

- Google email accounts purchased from QuickMail will now be re-authenticated automatically

### FIXES

- Accounts using unsecured custom domain tracking will no longer be able to purchase email accounts from QuickMail, as it was causing an error

## May 23, 2025

### FIXES

- The stats showing leads' email provider was flickering

- Events were not logged when a LinkedIn account’s 2FA is invalidated

- LinkedIn accounts were not being synced when added for the first time

### FIXES

- Purchased Google inboxes incorrectly counted toward the limit, preventing new inboxes from being added.

## May 15, 2025

### FIXES

- Leads in a campaign were running into an error due to LinkedIn proxy issue.

- Optimized issues with ordering a domain

## May 5, 2025

### FEATURES

- Ability to setup email forwarding when ordering a domain

### FIXES

- Users encountered issues when trying to order a domain because of a Cloud Identity problem.

- Accepted connection requests for LinkedIn was not being detected

## May 2, 2025

### FEATURES

- The workspace dashboard now shows the split distribution of leads' providers.

![screenshot](../images/026_file-9NKrAEC1yO.png)

### FIXES

- There was no audit log when the system failed to add a LinkedIn account via 2FA, making troubleshooting hard to figure out.

- Made adding LinkedIn accounts via 2FA more robust

- Buying new email accounts from QuickMail when the subscription’s inbox limit was already reached was failing. Email accounts purchased from QuickMail were not counting towards the subscription limit.

- Company name of the leads wasn’t showing up on the lead’s page of campaigns

## April 29, 2025

### FEATURES

- Support for adding LinkedIn accounts using LinkedIn credentials and 2FA for improved connection stability

## April 23, 2025

### FIXES

- When a user was added as a guest to an inactive account, they were unable to access other organizations they had been added to, as an error was being displayed.

- Fixed errors with ordering Google domains

- The warning icon for custom inboxes does not get updated immediately after reauthentication, which was causing confusion for users.

## April 21, 2025

### FEATURES

- Bulk actions are now available in Opportunities. This allows users to manage opportunities more easily and save time.

## April 17, 2025

### FIXES

- Some LinkedIn accounts can't be synced for new replies due to 500 error

- Images on some emails were being converted into an attachment

## April 14, 2025

### FEATURES

- Allow users to extract the number of available, active, and completed leads in a campaign via API

- Ability to extract how many leads run into an error via API

## April 7, 2025

### FEATURES

- Ability to manage Google Drive permissions in the new UI

- Ability to filter journeys based on the LinkedIn account they're assigned

### FIXES

- Improved tooltip when hovering over email addresses icon in Opportunities so users could easily see the recipient and sender's email address

## April 1, 2025

### FEATURES

- Reword emails with AI using different languages

## March 28, 2025

### FEATURES

- Ability to add leads to campaigns via API

### FIXES

- The list of campaigns in the agency dashboard was not showing paused campaigns by default

- When extracting the list of live campaigns via API, it led to an error

## March 18, 2025

### FEATURES

- When a lead accepted a connection request via LinkedIn, an opportunity is now created.

## March 8, 2025

### FIXES

- Replying to opportunities associated with a deleted account was leading to an error

- Users couldn’t change the recovery period for Deliverability AI
