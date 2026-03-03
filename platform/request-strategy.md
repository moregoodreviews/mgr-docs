---
description: Automate your review requests based on a strategy, or set of rules.
icon: chess-rook
---

# Request Strategy

Your request strategy controls when and how MGR sends review requests to your customers. Each project has its own strategy. You decide who gets asked, when they get asked, and how many follow-ups they receive. The goal is to request reviews at the right times from customers who are likely to leave positive feedback.

Go to **Settings** in the sidebar and select **Strategy** to view and edit your strategy.

### What It Does

The strategy is a set of rules that runs automatically. When a customer meets your conditions (for example, they signed up or were charged, and they have enough charge history), MGR waits for the delay you set, then sends the first review request. If they don't respond, reminders and retries can follow. Limits and schedules help you control volume and timing.

---

### Settings

#### Trigger

The trigger starts the process. Choose when the first request is sent:

* **Send request after a date** – Use the customer's signup or start date.
* **Send request after a charge** – Use the date of their most recent charge.

#### Delay

How long to wait after the trigger date before sending the first request. You can set the delay in hours, days, or months. For example, wait 14 days after signup, or 2 hours after a charge.

#### Channels

Choose how to reach customers: **Email**, **SMS**, or both. SMS requires an SMS connection and may be a paid add-on.

#### Thank You Messages

Enable or disable automatic thank-you messages when a customer leaves a review. When enabled, MGR sends a short thank-you over the same channel(s) you use for requests.

#### Message Link Expiration

Optionally expire the review link after a set number of days (3, 5, 7, 14, 30, 60, or 90). After that, the link no longer works. Leave this blank for no expiration.

---

### Reminders

If a customer doesn't click a rating in any of your emails or messages, you can send reminders. Choose how many reminders to send (0, 1, 2, or 3) and how many days to wait before each one.

* **One reminder** – Set a single delay (e.g., 2 days later).
* **Two or three reminders** – Set a separate delay for the first, second, and third reminder.

If you use both email and SMS, you can exclude one channel from reminders. For example, send reminders by email only and not by SMS.

{% hint style="info" %}
Reminders are a paid add-on on some plans. If the option is locked, you may need to upgrade.
{% endhint %}

---

### Retries

Retries are different from reminders. A **retry** is a new full request sequence sent to a customer who never clicked a rating in any of your previous requests or reminders. Use retries to give them another chance later.

Choose how many retries to send (0, 1, or 2) and how many days to wait after the last request before sending the next sequence.

{% hint style="info" %}
Retries are a paid add-on on some plans. If the option is locked, you may need to upgrade.
{% endhint %}

---

### Schedule

Control which days and times requests are sent. For each day of the week you can:

* **Send anytime** – Requests can go out any time that day.
* **Send between** – Choose a start and end time (e.g., 9:00 AM–5:00 PM).
* **Do not send** – No requests on that day.

Set a time zone so the schedule applies correctly for your customers.

---

### Conditions

Narrow who receives requests based on charge history and subscription status.

#### Require Subscription

When set to **Yes**, only customers with an active subscription receive requests. Customers without a subscription are skipped.

#### Charge Conditions

Target higher-value customers by setting minimums:

* **Number of charges** – Minimum number of charges (e.g., at least 3).
* **Total charge amount** – Minimum total amount charged (in your project currency).
* **Average charge amount** – Minimum average per charge (in your project currency).

Leave any field at 0 to skip that condition. All conditions you set must be met for a customer to receive a request.

---

### Limits

Cap how many requests go out per day or per month for email and SMS. This helps you stay within provider limits or control costs.

* **Daily email requests** – Max requests per day by email.
* **Monthly email requests** – Max requests per month by email.
* **Daily SMS requests** – Max requests per day by SMS.
* **Monthly SMS requests** – Max requests per month by SMS.

Leave a limit blank for no cap. Limits apply per project.

{% hint style="info" %}
Limits may only be visible to account owners. If you don't see this section, your plan or role may restrict it.
{% endhint %}

---

### How to Edit Your Strategy

1. Go to **Settings** in the sidebar.
2. Click **Strategy**.
3. Adjust the sections you need (Settings, Reminders, Retries, Schedule, Conditions, Limits).
4. Click **Save** in each section after making changes.

Changes apply to future requests. Customers already in the queue keep their existing schedule.

---

### Tips

{% hint style="info" %}
A customer is only automatically requested once per project. After that, you can manually send another request from the customer's page if you want to ask again.
{% endhint %}

{% hint style="success" %}
Start with a simple strategy—for example, 14 days after signup, email only, no reminders—and add conditions, reminders, or limits as you learn what works for your business.
{% endhint %}

{% hint style="warning" %}
If you use the "after a charge" trigger, make sure you're importing charge history from Stripe, an app connector, or the API. Without charge data, customers won't qualify.
{% endhint %}
