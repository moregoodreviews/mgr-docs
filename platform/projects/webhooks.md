---
description: Add webhooks to your project to receive events about reviews and messages.
icon: webhook
---

# Webhooks

Webhooks notify your systems when something happens in your project—for example, when a customer leaves a review or when a message is sent. You provide a URL, and the platform sends the relevant data to that URL as soon as the event occurs. This lets you sync reviews and messages with your own tools, dashboards, or workflows.

### Where to Find Webhooks

Go to **Settings** in the sidebar, then click **API**. Scroll to the **Webhooks** section. You can add one or more webhook URLs there. Each webhook receives all events for your project unless you choose to filter by event type.

### Adding a Webhook

1. In Settings > API, scroll to the Webhooks section.
2. Click **Create Webhook** (or **Add** if you already have webhooks).
3. Enter the full URL where you want to receive events. It must start with `https://`.
4. Click **Create**.

Your webhook is active immediately. You can turn it on or off anytime using the switch next to its URL. When a webhook is off, no events are sent to that URL.

### Event Types

Each webhook sends a notification when one of these events occurs:

| Event | When it fires |
|-------|---------------|
| **review-created** | A customer submits a rating or review (including when they first click a rating link). |
| **review-updated** | An existing review is updated (for example, the customer adds or edits their feedback). |
| **review-deleted** | A review is removed. |
| **message-created** | A review request message is created or scheduled. |
| **message-updated** | A message is updated (for example, when it is sent or delivered). |
| **message-deleted** | A message is removed or canceled. |

### Review Events: Created vs Updated

A review is created as soon as a customer clicks a rating link in an email or SMS. When they land on your review page, the rating is already saved—even before they type any text or submit the form. If they then add feedback or a written review in the form, that update triggers a second event.

So for a single customer visit, you may receive:

1. **review-created** – When they click the rating link and the page loads.
2. **review-updated** – When they submit the form with additional feedback or text.

{% hint style="info" %}
If you only need to know when a customer has finished their full review (including text), use the **review-updated** event. The **review-created** event fires when the rating alone is captured.
{% endhint %}

### What Your Endpoint Receives

Each notification includes the event type and the full data for that review or message. Your endpoint receives the data in a standard format and should respond quickly to confirm receipt. If your endpoint does not respond successfully, the platform will retry a few times. After several failed attempts, the webhook may be automatically turned off to avoid repeated errors.

{% hint style="warning" %}
Webhooks are a paid feature. If you don’t see the option to add webhooks, you may need to upgrade your plan.
{% endhint %}

### Managing Webhooks

* **Turn off** – Use the switch next to a webhook to pause it. No events are sent while it’s off. Turn it back on when you’re ready.
* **Edit** – Change the URL or choose which event types to receive. By default, a webhook receives all events. When editing, you can uncheck events you don’t need so only the relevant ones are sent.
* **Delete** – Remove a webhook from the actions menu when you no longer need it.

{% content-ref url="../api-reference.md" %}
API Reference
{% endcontent-ref %}
