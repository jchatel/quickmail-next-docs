# Connecting to QuickMail's MCP

You can now connect QuickMail to your favorite AI platform, such as Claude, ChatGPT, or Cursor, using the QuickMail MCP server. Once connected, you can ask your AI assistant to analyze your campaign performance, manage leads, and build campaigns in plain language.

The QuickMail MCP works just like the [QuickMail API](LINK_TO_API_ARTICLE). Anything you can do with the API, you can now do by chatting with your AI assistant, no coding needed.

> [!NOTE]
> MCP stands for Model Context Protocol. It is an open standard that lets AI assistants securely connect to apps like QuickMail.

## In this article

* [What you can do](#what-you-can-do)
* [Before you start](#before-you-start)
* [Create your API key](#create-your-api-key)
* [Connect QuickMail to Claude](#connect-quickmail-to-claude)
* [Connect QuickMail to ChatGPT](#connect-quickmail-to-chatgpt)
* [Connect QuickMail to Cursor](#connect-quickmail-to-cursor)
* [Rate limits](#rate-limits)
* [Tips for best results](#tips-for-best-results)
* [Troubleshooting](#troubleshooting)

## What you can do

Here are a few things you can ask your AI assistant once QuickMail is connected:

* "Show me the stats for my Q4 Outreach campaign."
* "How many leads are active, available, and completed in each of my campaigns?"
* "Which leads ran into an error this week?"
* "Clone my Partners campaign and rename it Partners 2026."
* "Create a new campaign with three email steps and a two day wait between each."
* "Tag every lead from Acme Inc. as Enterprise."

### Account and workspaces

* Get your agency name, ID, and URL
* List your workspaces with their IDs, names, and URLs
* Include or exclude specific workspaces when filtering

### Campaigns

* List campaigns with their IDs, names, and URLs
* View stats for a specific campaign
* Create, clone, and rename campaigns
* Update send times
* Turn campaign email verification on or off

### Campaign steps

* Create email steps
* Add email variations
* Create wait steps

### Email accounts

* Get email account IDs
* Assign or unassign email accounts to campaigns

### Leads

* Get lead details and search leads by tags
* See how many leads are available, active, or completed in a campaign
* Find leads that ran into an error
* Delete leads
* Cancel leads in a campaign (cancel journeys)
* Remove leads from a campaign (remove journeys)

### Tags and custom properties

* Create tags and assign them to leads
* Create custom properties and set their values

## Before you start

You will need:

* An active QuickMail account
* Your QuickMail API key
* An AI platform that supports remote MCP servers
* The QuickMail MCP server URL:

```
https://api.quickmail.com/mcp
```

## Create your API key

The MCP uses your QuickMail API key to access your account. If you don't have one yet, follow the steps in [Creating an API Key](LINK_TO_API_KEY_SECTION).

> [!WARNING]
> Your API key gives full access to your QuickMail account. Keep it private and never share it in public chats or documents.

## Connect QuickMail to Claude

1. Open [Claude](https://claude.ai) and go to **Settings** > **Connectors**.
2. Click **Add custom connector**.
3. Enter `QuickMail` as the name and paste the server URL.
4. Click **Add**, then click **Connect**.
5. When prompted, enter your QuickMail API key and approve access.

That's it! Start a new chat and ask Claude something about your QuickMail account.

> [!TIP]
> Custom connectors are available on Claude Pro, Max, Team, and Enterprise plans. On Team and Enterprise plans, an owner may need to add the connector first.

## Connect QuickMail to ChatGPT

1. Open ChatGPT and go to **Settings** > **Apps & Connectors**.
2. Turn on **Developer mode** under **Advanced settings**.
3. Click **Create** and paste the QuickMail server URL.
4. When prompted, enter your QuickMail API key and approve access.

## Connect QuickMail to Cursor

1. Open Cursor and go to **Settings** > **MCP**.
2. Click **Add new MCP server**, or add the following to your `mcp.json` file. Replace `YOUR_API_KEY` with your QuickMail API key.

```json
{
  "mcpServers": {
    "quickmail": {
      "url": "https://api.quickmail.com/mcp",
      "headers": {
        "Authorization": "Bearer YOUR_API_KEY"
      }
    }
  }
}
```

3. Save the file and restart Cursor.

## Other AI platforms

Most AI tools that support remote MCP servers work the same way. Look for a setting called **Connectors**, **Integrations**, or **MCP servers**, then add the QuickMail server URL and your API key.

## Rate limits

The QuickMail MCP follows the same rate limit as the API: **10 requests per 10 seconds**.

If you ask for a lot of data at once, such as stats across many campaigns, your assistant may need a little extra time. If you hit the limit, just wait a few seconds and try again.

## Tips for best results

* **Be specific.** Mention campaign names, workspaces, date ranges, or tags so your assistant finds the right data.
* **Review before you confirm.** Actions like deleting leads or canceling journeys can't be undone. Most AI platforms will ask for your approval before making changes.
* **Start small.** Try a few questions first, like "List my campaigns," to see how your assistant works with your data.

## Troubleshooting

**My assistant can't find the QuickMail tools.**
Make sure the connector is turned on for your current chat. In Claude, click the tools icon in the chat box and check that QuickMail is enabled.

**I see an authentication error.**
Check that your API key is correct and still active. If needed, create a new key and reconnect QuickMail.

**The results look incomplete.**
QuickMail returns large results in pages. Ask your assistant to "show the next page" or narrow your request to a specific campaign or workspace.

**I'm getting rate limit errors.**
Wait a few seconds, then try again. Breaking large requests into smaller ones also helps.

## Need help?

If you have any questions, reach out to our support team through the chat widget in your QuickMail dashboard. We're always happy to help!
