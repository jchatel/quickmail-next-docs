---
title: Company Colleagues Attribute
description: Use {{=company.colleagues}} to mention or CC a lead's colleagues from the same company in your emails.
---

# Company Colleagues Attribute

The `{{=company.colleagues}}` attribute automatically fills in the names of a lead's colleagues who belong to the same company or email domain.

## In this article

- [What is the company colleagues attribute?](#what-is-the-company-colleagues-attribute)
- [How does it work?](#how-does-it-work)
- [How to use it in an email](#how-to-use-it-in-an-email)
- [How to CC colleagues](#how-to-cc-colleagues)
- [Why am I getting an error?](#why-am-i-getting-an-error)
- [Things to keep in mind](#things-to-keep-in-mind)

## What is the company colleagues attribute?

`{{=company.colleagues}}` is a precomputed attribute. You don't need to fill in any values yourself. When the email is sent, QuickMail looks for other leads under the same company or domain and replaces the attribute with their names.

This is useful when you reach out to several people at the same company and want to let each person know who else you contacted.

## How does it work?

QuickMail groups leads by company or email domain. For example, if these leads are in your workspace:

| Lead | Email |
| --- | --- |
| Richard Hendricks | richard@piedpiper.com |
| Monica Hall | monica@piedpiper.com |
| Jared Dunn | jared@piedpiper.com |

When Richard receives an email that uses `{{=company.colleagues}}`, the attribute is replaced with the names of Monica and Jared, since they share the same company domain.

## How to use it in an email

Add the attribute to the body of any email step:

```
Hi {{lead.first_name}},

I also reached out to {{=company.colleagues}} since you all work on the product team at {{company.name}}.
```

When the email is sent to Richard, it will look like this:

```
Hi Richard,

I also reached out to Monica Hall and Jared Dunn since you all work on the product team at Pied Piper.
```

## How to CC colleagues

You can also add `{{=company.colleagues}}` to the **CC** field of an email step. This copies the lead's colleagues from the same company on the email.

> **Note:** If two or more leads from the same company are running the same campaign, each lead will receive their own email, and their colleagues will be CC'd on each one. This means the same people may receive several copies of similar emails.

## Why am I getting an error?

The colleagues attribute always tries to fill in a value. If a lead has **no colleagues** from the same company or domain in QuickMail, there is nothing to fill in. The email will not be sent, and the lead's journey will stop with an error.

This keeps emails from going out with an empty or broken placeholder.

## Things to keep in mind

- **Only use this attribute for leads who have colleagues.** Place leads who have colleagues in one campaign and leads without colleagues in a separate campaign that doesn't use the attribute. Tagging leads can help you keep them organized.
- **Colleagues are matched by company or domain.** Make sure your leads have the correct company and email address so they are grouped correctly.
- **Test before launching.** Send a test email to check how the colleague names appear before starting the campaign.
