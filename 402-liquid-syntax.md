# Personalizing Emails with Liquid Syntax

In this article:

- What is liquid syntax?
- Why use liquid syntax?
- How to use liquid syntax?
- Examples
- I can't save my liquid syntax, what's wrong?
- How to check how my liquid syntax will transform?

## What is liquid syntax?

Liquid syntax is a templating language created by Shopify and widely used in many apps, including QuickMail, to personalize content.

For a detailed documentation of it, please go to this link: https://shopify.github.io/liquid/basics/introduction/

## Why use liquid syntax?

Liquid syntax allows you to highly personalize and create dynamic emails based on the leads' info, tags, and attributes.

It lets you:

- Add personalization without needing perfect data
- Segment messaging without building extra campaigns
- Build smarter follow-ups with conditional logic

## How to use liquid syntax?

Liquid uses a combination of objects, tags, and operators.

The format should look like this:

```
{% if lead.role == "CEO" %} As a founder, I would like to offer you this one-time promotion {% endif %}
```

So if the email is sent to a prospect with the role of a CEO, the email will contain "*As a founder, I would like to offer you this one-time promotion*". Otherwise, the texts won't appear in the email.

### Tags

Tags are the curly brace percentage delimiters `{%` and `%}`. It denotes logic and control flow.

### Objects

**Important:** The value of the object in the liquid syntax is case-sensitive.

Objects contain the content that liquid displays on the email. Here are the available objects and their functions in QuickMail:

| Object | Function |
| --- | --- |
| lead.first_name | First Name |
| lead.last_name | Last Name |
| lead.email | Email |
| lead.title | Title |
| lead.role | Role |
| lead.phone | Phone |
| lead.linkedin | LinkedIn |
| lead.score | Score |
| lead.custom.customfieldsname | Custom Fields |
| company.name | Company Name |
| company.domain | Company Domain |
| inbox.name | Inbox Name |
| inbox.friendly_name | Inbox Friendly Name |
| inbox.email | Inbox Email |
| inbox.signature | Inbox Signature |
| lead.tag.tagname | Tag |

### Operators

| Operator | Function |
| --- | --- |
| != | Is not equal |
| == | Equals |
| > | Greater than |
| < | Less than |
| >= | Greater than or equal to |
| <= | Less than or equal to |
| or | Condition A or Condition B |
| and | Condition A and Condition B |
| contains | Condition A |

## Examples

**Important:** Using custom properties and tags in Liquid syntax is case-sensitive.

### Fallback when data is missing

```
{% if lead.first_name == "" %}
Hi there,
{% else %}
Hi {{lead.first_name}},
{% endif %}
```

### Different email content based on different tags

```
{% if lead.tag.vip == true %}
  Hey VIP!
{% elsif lead.tag.new_lead == true %}
  Welcome aboard!
{% elsif lead.tag.long_time_customer == true %}
  Great to see you again!
{% else %}
  Hi {{lead.first_name}}!
{% endif %}
```

### Different email content based on different lead properties

```
{% if lead.role == "Founder" or lead.role == "CEO" %}
Hi {{lead.first_name}},

Reaching out directly since you're leading the company.
I'll keep this short.

We're helping founders get more replies from cold outreach without harming deliverability.

{% elsif lead.role != "" %}
Hi {{lead.first_name}},

Not sure if outreach falls under your role as a {{lead.role}}, but thought this might still be useful for your team.

{% else %}
Hi there,

I couldn't find your role, so keeping this general—this might still help if your team handles outbound.
{% endif %}
```

### Different email content based on number operators

**Important:** In QuickMail, all variables (like *lead.score*) are stored as strings, even if they look like numbers.

Because of this:

- You cannot directly use numeric comparison operators (like >, <, >=, <=) on these variables.
- To perform numeric comparisons, you must first convert the string to a number.

You can use the `{% assign %}` tag combined with the *plus* filter to convert a string to a number.

For example:

```
{% assign score_num = lead.score | plus: 0 %}
```

So if you want to have different email content based on a number assigned to leads, it should be like this:

```
{% assign score_num = lead.score | plus: 0 %}
{% if score_num >= 80 %}
Hi {{ lead.first_name | default: "there" }},

You're one of our top prospects! Let's schedule a call to discuss how we can help you grow.

{% elsif score_num >= 50 and score_num < 80 %}
Hi {{ lead.first_name | default: "there" }},

Thanks for your interest so far. If you want, I can share some resources tailored to your needs.

{% elsif score_num < 50 and score_num > 0 %}
Hi there,

I wanted to reach out and introduce myself. If you have any questions, feel free to reply.

{% else %}
Hi there,

Still getting to know where you're at, but happy to connect if you're curious!
{% endif %}
```

## I can't save my liquid syntax, what's wrong?

If you can't save the liquid syntax, it could be that the feature is not turned on for your plan yet.

Please reach out to support@quickmail.io to double-check.

Liquid syntax can't be saved as well if it's incorrect.

Please make sure your liquid is using the correct properties and tags, and that the case is correct.

If you get stuck, you can use AI tools like [ChatGPT](https://chatgpt.com/) to double-check your syntax.

## How to check how my liquid syntax will transform?

You can send test emails to test out your liquid syntax.

Check out this article for a detailed guide on sending test emails.
