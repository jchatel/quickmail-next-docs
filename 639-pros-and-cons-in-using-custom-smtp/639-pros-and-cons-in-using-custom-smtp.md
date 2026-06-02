# Pros and Cons in using Custom SMTP

**

Using a custom SMTP service to send emails from QuickMail has both benefits and drawbacks. Here are some of them:

## Pros:

- Sending can be less risky when using an SMTP provider like SendGrid, Mailgun, or Postmark.

- It provides an additional backup for your client. For example, if your primary inbox provider (like G Suite or Outlook) doesn’t handle the sending, it reduces the risk of being blocked. This ensures your client can continue using their email normally, even with ongoing cold email activities.

- Bounces are handled at the provider level, preventing them from appearing in your client’s inbox.

- Sending higher email volumes can be less problematic compared to using a standard G Suite inbox.

## Cons:

- Cold emailing is generally against the policies of most SMTP providers, so there is a risk of account termination without much warning (similar to G Suite blocking you).

- Since bounces don’t land in inboxes, QuickMail won’t detect them, which means follow-up emails may still be sent to addresses that have already bounced.

- You’ll need to test open tracking, click tracking, and unsubscribe functions to ensure they work correctly. In some cases, tracking features may interfere with QuickMail’s tracking, but this is usually due to a misconfiguration and can be fixed.

- Deliverability can vary significantly. There’s a higher chance of emails landing in the **Promotions** tab unless you set up white-labeling (which is highly recommended). However, white-labeling requires DNS changes, which can be tricky for some clients.

- Most SMTP services use shared IPs. If you want a dedicated IP (which helps with monitoring complaints and managing sender reputation), it comes at an additional cost.
