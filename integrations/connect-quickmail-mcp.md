# Connecting to QuickMail's MCP 🤖

QuickMail's MCP now lets you connect your account to AI platforms like Claude and ChatGPT! Once connected, you can use AI to get insights from your campaigns, manage your leads, create campaigns, and handle other QuickMail tasks without writing code.

## In this article

* [How does it work?](#how-does-it-work)
* [What can you do with QuickMail's MCP?](#what-can-you-do-with-QuickMails-mcp)
* [IMPORTANT: Before you start](#before-you-start)
* [How to connect QuickMail's MCP to Claude](#connect-to-connect-quickmail's-mcp-to-claude)
* [Troubleshooting](#troubleshooting)

## How does it work? 

QuickMail's MCP connects your AI assistant to your QuickMail account, allowing it to retrieve information and perform supported actions through QuickMail's API.

Once connected, you can simply tell your AI assistant what you need in plain language. It can then fetch the relevant data or carry out the action for you, without requiring you to write code.

For example, you can ask:
"Show me the performance of my Q4 Outreach campaign."

Your AI assistant can retrieve the campaign data from QuickMail and present the results to you.

## What can you do with QuickMail's MCP?

With QuickMail connected, your AI assistant can help you work with your campaigns and leads, answer questions about your data, and perform specific campaign-related actions.

Here are some of the things you can do:
- Get campaign statistics, such as opens, clicks, replies, and bounces
- Analyze your campaign data and ask questions about your outreach
- Create, clone, and rename campaigns
- Create and delete leads
- Add, cancel, and remove leads in campaigns
- Search for leads by name, email, phone, or LinkedIn ID
- Create tags and assign them to leads
- Create and update email, wait, and LinkedIn steps
- Update campaign send times and email verification settings
- Assign email accounts to campaigns and set custom tracking domains
- Access workspace and account information
- Create and update custom lead properties
- Retrieve other data and perform other actions supported by the QuickMail API

## ⚠️ Before you start 
You'll need:
* An AI app that supports remote MCP servers with OAuth sign-in. A paid AI subscription may be required, depending on the app.
* Your QuickMail login and access to the organization you want to connect
* API access enabled for that QuickMail organization

You'll sign in with your regular QuickMail account, so there's no need to create or paste an API key.

## How to connect QuickMail's MCP to Claude?

**Step 1.** Go to Claude Settings → Connectors → +Add → Add custom connector


<img width="1032" height="759" alt="image" src="https://github.com/user-attachments/assets/6ea9365b-854f-4a15-a3ad-a881da5a74a2" />


**Step 2.** Enter the following details and click 'Continue'

* **Name:** QuickMail 
* **Server URL:** https://api.quickmail.com/mcp

<img width="1029" height="750" alt="image" src="https://github.com/user-attachments/assets/3a68a2aa-fcb8-4311-8453-6f3117da7506" />

**Step. 3** Follow the on-screen instructions. Select the following settings and then click 'Add'
* **Authentication:** Sign in now
* **OAuth client:** Register Automatically

<img width="1022" height="751" alt="image" src="https://github.com/user-attachments/assets/26cc9b33-10b0-44e8-894a-38f9c452cc32" />

**Step. 4** Connect your QuickMail account. Make sure to select the correct organization (if you're managing multiple organizations)

<img width="823" height="528" alt="image" src="https://github.com/user-attachments/assets/719e1b3f-851f-471e-9d19-9ce97ca05152" />

**Step. 5** You'll be redirected to your Claude Settings. To confirm whether you've successfully connected, you'll see QuickMail in the list of connectors. 

<img width="1233" height="796" alt="image" src="https://github.com/user-attachments/assets/601b974e-36e6-48c2-9958-5ece2552eb1a" />

## Troubleshooting

### The connection does not start
Check that the server URL is exactly https://api.quickmail.com/mcp and that your app supports remote MCP with OAuth. Use OAuth sign-in rather than an API key or manual authorization header.

### I opened the URL and got an error
The server URL is for your AI app’s connector settings. It is not a web page. Paste it into the connector setup to begin.

### My organization is missing or access is denied
Check that you signed in to the correct QuickMail account and still have access to the organization. Your organization must also have API access enabled.

### I can read data but cannot make changes
Check your workspace permissions with your organization administrator. Read-only guest access does not allow updates or deletions.

### The connection stopped working
Reconnect to sign in again. If that does not resolve it, check whether your QuickMail account, organization, or workspace access has changed.

### I get a “Too many requests” error
Wait briefly, then try again. MCP uses the same organization request limit as the QuickMail API.

For available API fields and operations, see the [API v2 documentation](https://help.quickmail.com/integrations/setting-up-api-v2/).



