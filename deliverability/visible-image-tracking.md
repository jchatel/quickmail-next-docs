# Visible Image Tracking

In addition to the ability todisable open tracking based on email provider that we recently launched, we’ve added a new QuickMail feature that allows users to track opens based on the images they include, helping to prevent emails from being flagged for open tracking.

This update responds to Gmail now flagging emails with hidden images, including tiny pixels used for open tracking in cold outreach. Recipients see a banner stating, “Images in this message are hidden,” along with a prominent “Report spam” button, which could decrease reply rates and increase spam reports

![screenshot](../images/000_file-0gHsUOu8oi.png)

## How does it work?

By default, QuickMail inserts a tiny, invisible tracking pixel into your emails. When the recipient opens the email, this pixel loads, signaling that the email has been read.

With Visible Image Tracking, we will use any visible images you include in your emails to track opens, helping to prevent the email from being flagged.

If you don’t include an image, we will insert a tiny transparent dot at the bottom of the email. While this dot is invisible to the eye, it remains detectable in the HTML code. This approach ensures that the warning message does not appear for recipients.

**Important:** Visible image tracking only works for "linked images" or those added via an image UR, not for embedded or directly uploaded images in the email.

## How to set it up?

Go to your workspace settings → General → Check the box labeled Image Tracking**. Once enabled, the feature will take effect immediately.

![screenshot](../images/001_file-S5QvMcOCQE.png)
