---
description: >-
  Connect Claude and other AI assistants to your project to manage customers,
  reviews, ratings, feedback, and reputation through natural conversation.
icon: robot
---

# MCP Server

The **MCP Server** lets you connect AI assistants like **Claude** to your project so you can ask them to look up customers, send review requests, search reviews, organize tags and locations, and follow up on feedback—all in plain English. Instead of clicking through screens, you describe what you want and your assistant does it for you using your project's data.

MCP stands for **Model Context Protocol**, a standard way for AI assistants to plug into outside tools. We host an MCP server for your project so any assistant that supports MCP can connect securely.

{% hint style="info" %}
You don't need to copy or paste an API key. Connecting is done through a normal sign-in screen, the same way you'd sign in to any other app.
{% endhint %}

***

## What you can do once connected

Once Claude (or any MCP-compatible assistant) is connected to your project, you can ask it to do things like:

* **Find and update customers** — "Find John Smith and add the VIP tag" or "Show me everyone in the Brooklyn location who hasn't been asked for a review yet."
* **Send review requests** — "Email a review request to the five customers I added this week."
* **Search and report on reviews** — "How many five-star reviews did we get last month?" or "Show me any one-star reviews from the last 30 days that haven't been replied to."
* **Reply and follow up** — "Draft a reply thanking everyone who left a five-star review yesterday."
* **Organize your project** — "Create a new tag called 'Holiday Promo' and add it to anyone who reviewed in December."
* **Manage locations and sources** — "List my locations and how many reviews each one has."

Anything you can do on the project's own screens—working with customers, review requests, reviews, ratings, messages, locations, sources, and tags—your assistant can do on your behalf once it's connected.

***

## Connect Claude to your project

The exact menu names change as Claude updates, but the steps are the same in Claude desktop and on **claude.ai**.

1. Open Claude and go to **Settings**.
2. Find the **Connectors** (sometimes called **Integrations**) section.
3. Choose **Add custom connector**.
4. Give it a name like **More Good Reviews**.
5. Paste this URL into the server field:

```
https://api.moregoodreviews.com/mcp
```

6. Save the connector. Claude will open a sign-in window.
7. Sign in to your More Good Reviews account if you aren't already.
8. On the **Authorize** screen, pick the project you want Claude to work with, review the permissions, and choose **Authorize**.

You'll be sent back to Claude and the connector will show as connected. From your next message, Claude can use it.

{% hint style="success" %}
You only need to authorize once per project. To switch projects later, disconnect the connector and add it again, then choose a different project on the **Authorize** screen.
{% endhint %}

{% hint style="info" %}
If you belong to more than one project, the **Authorize** screen lists every project you're allowed to open. Pick the one you want Claude to work with for this connection.
{% endhint %}

***

## Try it out

Once Claude is connected, copy any of these prompts into the chat to see the connector at work:

1. **Catch up on this week's feedback**

> "Using More Good Reviews, summarize every review left in the last 7 days. Group them by rating and call out anything I should reply to first."

2. **Send a batch of review requests**

> "In More Good Reviews, find the customers I added this month who haven't been asked for a review yet, and email them a review request."

3. **Find at-risk customers**

> "Show me any one or two-star reviews from the last 30 days that haven't been replied to yet, with the customer name and what they said."

4. **Tag and organize a group**

> "Create a tag called 'Holiday 2025' in More Good Reviews and add it to every customer who left a review in December."

5. **Get a quick report on a location**

> "List my locations in More Good Reviews and tell me how many reviews and the average rating each one has over the last 90 days."

Claude will use the connector, fetch the answer from your project, and reply in the chat. You can keep going from there—asking follow-up questions, sending more requests, or drafting replies—without leaving the conversation.

{% hint style="info" %}
Claude will sometimes ask for confirmation before doing something that changes your project, like creating customers, sending review requests, or deleting items. You can review what it's about to do and approve or cancel.
{% endhint %}

***

## Permissions

When you authorize Claude, you grant three levels of permission to your project:

* **Read** — look up customers, reviews, ratings, messages, locations, sources, and tags.
* **Write** — create or update customers, send review requests, reply to reviews, and edit project records.
* **Delete** — remove customers, reviews, tags, and other records.

These permissions apply only to the **single project** you picked on the Authorize screen. Claude can't see your other projects, your account settings, or anything in your agency unless you connect those separately.

{% hint style="warning" %}
Connecting an AI assistant means it can act on your project on your behalf. Only authorize assistants you trust, and review what they're about to do before approving destructive actions like deleting customers or reviews.
{% endhint %}

***

## Other MCP-compatible assistants

The MCP Server isn't only for Claude. Any tool that supports MCP can connect using the same URL and the same sign-in flow. If you use a different assistant that supports custom MCP connectors, paste the URL above into its connector settings and it will walk you through the same authorization screen.

***

## Disconnect

You can disconnect at any time, and there are two places to do it.

**From the AI assistant.** In Claude (or another MCP client), open **Settings**, find the More Good Reviews connector, and remove it. The assistant will stop having access immediately.

**From your account.** If you suspect a connection has been misused, you can also revoke it from your More Good Reviews account on any device. Removing the connector from the assistant is enough for normal cleanup.

After disconnecting, your reviews, customers, ratings, and feedback in the project are not affected—the assistant simply loses access. You can connect it again later by repeating the **Authorize** flow.

***

## Tips

{% hint style="success" %}
Tell your assistant the project name in your first message, like "in More Good Reviews, find …". This helps it remember to use the connector instead of guessing.
{% endhint %}

{% hint style="info" %}
For repeatable tasks—like a weekly summary of new five-star reviews or a monthly review-request batch—save the prompt in your assistant so you can run it again with one click.
{% endhint %}

{% hint style="warning" %}
Free or trial AI assistants sometimes limit how much data they can read in one go. If you ask Claude for "every review ever" and it stops early, narrow the request—for example, "the last 30 days" or "the last 100 reviews."
{% endhint %}

***

## Related documentation

* [AI Assistant](ai-assistant.md) — More Good Reviews' built-in AI for replying to reviews and writing message copy.
* [Integrations](integrations.md) — connect More Good Reviews with Google, Slack, Stripe, HubSpot, and more.
* [API Reference](api-reference/) — direct API access for developers building custom workflows.
* [Webhooks](projects/webhooks.md) — get notified in your own systems when reviews and other events happen.
