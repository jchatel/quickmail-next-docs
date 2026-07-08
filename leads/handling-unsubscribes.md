# Handling Unsubscribes

**In this article:**

- Why manually mark a lead as Do Not Contact?

- How to mark a lead as Do Not Contact?

  - Via Exclude list
  - Individually / Manually
  - In bulk

## Why Mark a Lead as Do Not Contact?

**When a lead clicks an unsubscribe link in your email, QuickMail automatically marks the journey as unsubscribed and adds the lead to the Do Not Contact list**. Leads on the Do Not Contact list cannot be added to any campaign.

**Pro tip:** To learn how to add an unsubscribe link to your emails, check out this article.

There are cases where you may need to do this manually, such as:

- Your emails do not have an unsubscribe link.

- A lead replied with the word "unsubscribe" instead of clicking the link. Only unsubscribe link clicks are supported at the moment.

- The lead unsubscribed from a different platform and you need to reflect that in QuickMail.

- You have a master list of unsubscribed leads and want to add them to QuickMail.

## How to Mark a Lead as Do Not Contact?

Leads can be marked as Do Not Contact individually or in bulk.


### Option 1 - Adding email addresses, domains, or LinkedIn profile IDs to the Exclude List

Go to the **List** page → Ellipsis → Exclude

<img width="1158" height="697" alt="image" src="https://github.com/user-attachments/assets/c4296dc8-36a8-403e-940a-81c364689900" />

After that go to either the Domain tab, Email Address tab, or LinkedIn tab and then click + Add at the upper right hand corner.

<img width="1161" height="695" alt="image" src="https://github.com/user-attachments/assets/66b23975-89fb-4754-ae13-b0c4e109e274" />


### Option 2 - Individually/Manually

Go to the **List** page → search for the lead → select the lead → **Actions** → **Mark as Do Not Contact**.

<img width="995" height="620" alt="image" src="https://github.com/user-attachments/assets/3e09e94d-2655-4f63-b1c3-4e5c2ea1bf58" />


You can also mark a lead as Do Not Contact from their quick view. To open it, click the preview button next to the lead's email address or click their thumbnail.

From the quick view, click the menu icon (three vertical dots) in the top-right corner → **Do Not Contact**.

<img width="1153" height="700" alt="image" src="https://github.com/user-attachments/assets/790e49b6-a9eb-43d9-a936-edd56e4b8168" />

**Pro tip:** The quick view is accessible from any page where leads appear, including the List page, Campaign Journeys, Sent Emails, and Tasks.


### Option 3 - In Bulk via Import

To bulk mark leads as Do Not Contact, you first need to tag them so they can be filtered.

**Step 1.** Create a tag by going to **List** → **Tags** → **Create New Tag**.

<img width="1155" height="696" alt="image" src="https://github.com/user-attachments/assets/a6d1b030-2d79-425e-9c57-60ddcd781281" />

Name the tag and save it. "DoNotContact" is just an example — you can name it anything.

**Note:** Tag names can only contain letters, numbers, hyphens (-), and underscores (_). Names with spaces cannot be created.

**Step 2.** Update your CSV by adding a column for Do Not Contact and entering "x" for every lead that should be marked.

![screenshot](../images/005_file-AlPZoarLMC.png)

**Step 3.** Import the updated CSV into QuickMail. Before clicking **Import**, make sure to map the DoNotContact column to the corresponding tag in QuickMail.

<img width="1160" height="694" alt="image" src="https://github.com/user-attachments/assets/e0c0b319-2a64-45fe-b47d-6366caff35c4" />

If you'd like to know more about using tags, check out this article: https://help.quickmail.com/leads/segmenting-leads-with-tags/

**Note:** If the leads already exist in QuickMail, make sure to check **Update lead if it exists**. Without this, existing leads will be rejected to prevent duplicates.

<img width="1158" height="693" alt="image" src="https://github.com/user-attachments/assets/16cce52b-4982-4683-aa23-72537c496a4b" />

**Step 4.** Once the import is complete, filter leads by the DoNotContact tag. Go to the **List** page → **Advanced Filter** → **Tags** → under **Has ANY of the following tags**, select **DoNotContact** → **Apply Filter**.

<img width="1161" height="697" alt="image" src="https://github.com/user-attachments/assets/40b14596-6291-4e58-b86a-0cdbc7ad18b3" />


**Step 5.** Select all filtered leads → **Actions** → **Mark as Do Not Contact**.

<img width="1160" height="697" alt="image" src="https://github.com/user-attachments/assets/f8fae606-7d36-4463-b8e7-7559c9e35b8c" />: 

**Pro tip:** You can also mark an entire domain as Do Not Contact by adding it to the DNC domain list.
