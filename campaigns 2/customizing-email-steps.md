# Customizing Email Steps

**In this article:**

- How do I change font type and sizes?

- How do I resize an image in the email editor?

- Can I use HTML?

- Can I add personalized images?

# How do I change font type and sizes?

At the moment, we don't support highly formatted emails.

This is mainly because highly formatted emails tend to get filtered more often than emails with plain text.

Due to this, the email editor has limited options for formatting and the options don't include changing font types and sizes, except for different headers.

# How do I resize an image in the email editor?

It's not possible to resize an image within QuickMail so it would be best to make sure that the images are resized before pasting them on the email step.

These articles might come in handy when resizing an image on [Windows](https://www.businessinsider.com/how-to-resize-an-image-on-windows) and [Mac](https://www.businessinsider.com/how-to-resize-an-image-on-mac).

# Can I use HTML?

The email editor doesn't support HTML yet; however, there is a workaround and it is to use custom properties.

To create a new property, go to the leads page and import a CSV or Drive.

![screenshot](../images/000_file-QkdjlgqCru.png)

**Note: You don't need to complete the import to create a custom property so you can load any CSV.**

Just go to the custom properties tab -> add a custom property.

![screenshot](../images/001_file-Fa67KAj19H.png)

Then, name your custom attribute -> paste the HTML code as the default value -> confirm.

![screenshot](../images/002_file-GSRW1zMrnE.png)

**Warning:** The custom property name should only contain alphanumeric characters, as well as - and _. Creating a custom property name that has a space will lead to an error.

![screenshot](../images/003_file-Wt5prGXnGk.png)

**Note:** Make sure that the HTML code is finalized before pasting it as a default value of the custom property because there's no option to edit an HTML code.

After creating the custom properties, just insert it into the email step.

Then, the HTML body will be translated once the prospect receives the email.

Here's how to do that:

![screenshot](../images/004_file-xr6bJbuZBR.png)

**Pro tip: You can personalize your emails using properties. Learn more about that ****here****.**

# Can I add personalized images?

Yes, you can!

We have an integration with Hyperise that you can use to create personalized images.

Learn more about setting it up [here](https://support.hyperise.com/email-marketing-integrations/quickmail-integration).
