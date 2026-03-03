---
description: >-
  Configure SMS templates for sending review requests and reminders to customers
  by text message. Customize message content for each template type.
icon: mobile-screen
---

# SMS Settings

SMS settings control the text messages your project sends to customers when requesting reviews. You can customize the message content for each type of SMS—requests, reminders, and thank-you messages. SMS is a paid add-on and requires an integration with an SMS provider before you can send messages.

### Where to Find SMS Settings

Go to **Settings** in the sidebar, then click **SMS**. You'll see the **Templates** section. If SMS is not enabled for your project, the section may be locked—upgrade or contact support to unlock it.

{% hint style="info" %}
Before you can send SMS, you must connect an SMS provider. MGR supports [Twilio](../sms/sms-with-twilio.md), [SimpleTexting](../sms/sms-with-simpletexting.md), and [ClickSend](../sms/sms-with-clicksend.md). Set up your integration in **Settings > Integrations**.
{% endhint %}

---

### Templates

SMS templates are the text messages your customers receive. Each template has a purpose:

* **Request** – The first message asking a customer to leave a review.
* **Reminder** – Follow-up messages sent when a customer hasn't responded yet. You can have up to three reminders, depending on your [Request Strategy](../request-strategy.md).
* **Thanks (positive)** – Sent when a customer leaves a positive rating.
* **Thanks (negative)** – Sent when a customer leaves a negative rating.

#### Editing a Template

1. Use the dropdown at the top to select which template you want to edit.
2. Edit the **Body** of the message. SMS messages are plain text—no subject line or formatting. You can use placeholders that get replaced with real data—for example, the customer's first name, your business name, or the link to leave a review.
3. Click **Save** to apply your changes.

{% hint style="info" %}
Placeholders like `{{first_name}}` and `{{project_name}}` are replaced automatically when the message is sent. Use them to personalize your texts and improve response rates.
{% endhint %}

{% hint style="warning" %}
SMS messages have character limits. Keep your messages short—a single standard SMS is 160 characters. Longer messages may be split into multiple segments and can cost more depending on your provider.
{% endhint %}

---

### How SMS Works With Your Strategy

SMS templates are used when your [Request Strategy](../request-strategy.md) is set to send via **SMS** or **both Email and SMS**. In the strategy:

* **Channels** – Choose SMS (or both) to enable SMS for your project.
* **Reminders** – You can exclude SMS from reminders if you prefer to send reminders by email only.
* **Throttles** – Set daily and monthly limits for SMS requests to control volume and costs.

{% hint style="success" %}
SMS can be more effective than email for reaching customers quickly. Many people open text messages within minutes. Combine SMS with email for the best results—customers who don't respond to email may respond to a text.
{% endhint %}

---

### Tips

{% hint style="info" %}
Keep SMS messages brief and direct. Include the customer's name and a clear call-to-action. Short, personal messages tend to get replies.
{% endhint %}

{% hint style="info" %}
When using both email and SMS, you can use different wording for each channel. SMS templates are separate from email templates—customize them for the shorter format.
{% endhint %}

{% hint style="success" %}
Review your SMS templates before enabling SMS in your request strategy. Make sure the review link placeholder is included so customers can tap through to leave feedback.
{% endhint %}
