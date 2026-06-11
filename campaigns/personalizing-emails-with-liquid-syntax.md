# Personalizing Emails with Liquid Syntax

**In this article:**

- What is liquid syntax?

- Why use liquid syntax?

- How to use liquid syntax?

- Examples

  - Fallback when data is missing

  - Different email content based on different tags

  - Different email content based on different lead properties

  - Different email content based on number operators

- I can't save my liquid syntax — what's wrong?

- How to check how my liquid syntax will transform?

## What Is Liquid Syntax?

Liquid syntax is a templating language created by Shopify and widely used in many apps, including QuickMail, to personalize content.

For detailed documentation, visit: [https://shopify.github.io/liquid/basics/introduction/](https://shopify.github.io/liquid/basics/introduction/)

## Why Use Liquid Syntax?

Liquid syntax allows you to create highly personalized, dynamic emails based on lead information, tags, and properties.

It lets you:

- Add personalization without needing perfect data

- Segment messaging without building extra campaigns

- Build smarter follow-ups with conditional logic

## How to Use Liquid Syntax?

Liquid uses a combination of objects, tags, and operators. The format looks like this:

```liquid
{% if lead.role == "CEO" %} As a founder, I would like to offer you this one-time promotion {% endif %}
```

If the email is sent to a lead with the role of CEO, the email will contain "As a founder, I would like to offer you this one-time promotion." Otherwise, the text will not appear.

### Tags

Tags use the `{%` and `%}` delimiters and are used to denote logic and control flow.

### Objects

**Important:** Object values in liquid syntax are case-sensitive.

Objects contain the content that Liquid inserts into the email. Here are the available objects in QuickMail:

| **Object** | **Function** |
|---|---|
| `lead.first_name` | First name |
| `lead.last_name` | Last name |
| `lead.email` | Email |
| `lead.title` | Title |
| `lead.role` | Role |
| `lead.phone` | Phone |
| `lead.linkedin` | LinkedIn |
| `lead.score` | Score |
| `lead.custom.customfieldsname` | Custom fields |
| `company.name` | Company name |
| `company.domain` | Company domain |
| `inbox.name` | Inbox name |
| `inbox.friendly_name` | Inbox friendly name |
| `inbox.email` | Inbox email |
| `inbox.signature` | Inbox signature |
| `lead.tag.tagname` | Tag |

### Operators

Operators are used to create conditions or fallbacks.

| **Operator** | **Function** |
|---|---|
| `!=` | Is not equal |
| `==` | Equals |
| `>` | Greater than |
| `<` | Less than |
| `>=` | Greater than or equal to |
| `<=` | Less than or equal to |
| `or` | Condition A or Condition B |
| `and` | Condition A and Condition B |
| `contains` | Condition A contains a value |

## Examples

**Important:** Custom properties and tags used in liquid syntax are case-sensitive.

### Fallback When Data Is Missing

```liquid
{% if lead.first_name == "" %}
Hi there,
{% else %}
Hi {{lead.first_name}},
{% endif %}
```

### Different Email Content Based on Different Tags

```liquid
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

### Different Email Content Based on Different Lead Properties

```liquid
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

I couldn't find your role, so keeping this general — this might still help if your team handles outbound.
{% endif %}
```

### Different Email Content Based on Number Operators

**Important:** In QuickMail, all variables (such as `lead.score`) are stored as strings, even if they look like numbers. Because of this:

- Numeric comparison operators (`>`, `<`, `>=`, `<=`) cannot be used directly on these variables.

- To perform numeric comparisons, you must first convert the string to a number using the `{% assign %}` tag combined with the `plus` filter.

For example:

```liquid
{% assign score_num = lead.score | plus: 0 %}
```

To use different email content based on a lead's score:

```liquid
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

## I Can't Save My Liquid Syntax — What's Wrong?

There are two possible reasons:

- **The feature is not enabled for your plan.** Reach out to [support@quickmail.io](mailto:support@quickmail.io) to confirm.

- **The syntax is incorrect.** Make sure you are using the correct properties and tags, and that the casing is right. If you get stuck, you can use an AI tool like [ChatGPT](https://chatgpt.com/) to help check your syntax.

## How to Check How My Liquid Syntax Will Transform?

You can send a test email to see how your liquid syntax renders. Check out this article for a detailed guide on sending test emails.
