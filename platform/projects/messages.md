---
description: >-
  View and manage review requests and reminders sent to customers by email or
  SMS. Track delivery, opens, and clicks.
icon: paper-plane
---

# Messages

Messages are the emails and SMS you send to customers to request reviews. Every request and reminder from your project appears here. You can see what was sent, when it was scheduled or delivered, and whether customers opened or clicked through. Messages also appear on each customer's profile so you can see the full history for one person.

### Where to Find Messages

**Project view** – Click **Messages** in the sidebar. You'll see all messages across your project, with summary stats at the top and a filterable table below.

**Customer view** – Open a customer's profile and scroll to the **Messages** section. You'll see only that customer's messages, grouped by request or in a flat list.

---

### Project Messages Page

The project Messages page shows every review request and reminder sent from your project. At the top, you'll see four summary numbers: **Sent**, **Opened**, **Clicked**, and **Failed**. Each number is a link—click it to filter the table to that status.

#### Filters

Use the toolbar to narrow what you see:

* **Search** – Search by customer name or other text.
* **Location** – If you have multiple locations, filter to one or leave as "All".
* **Channel** – Email, SMS, or both.
* **Template** – Request, Reminder, Thanks (positive), or Thanks (negative).
* **Status** – Scheduled, Sent, Opened, Clicked, Failed, or Complained.
* **Sort** – By date sent, date scheduled, date opened, or date clicked.

#### The Table

Each row is one message. You'll see:

* **Customer** – Name and avatar. Click the row to go to that customer's profile.
* **Channel** – Email or SMS.
* **Template** – The type of message (request, reminder, thanks).
* **Scheduled / Sent** – When it was scheduled or when it was actually sent.
* **Sent** – Whether the message was delivered.
* **Opened** – Whether the customer opened it (email only).
* **Clicked** – Whether the customer clicked through to leave a review.
* **Failed** – Whether the message failed to send, with a reason if available.

Click a row to open the customer's profile. The page scrolls to that message so you can see it in context with their other messages and reviews.

#### Bulk Actions

Select one or more messages using the checkboxes. When you have messages selected, a **Select bulk action** menu appears. You can **Cancel unsent messages** for all selected rows. This only works for messages that haven't been sent yet.

{% hint style="info" %}
Messages are created automatically when your request strategy runs. To schedule messages for a customer, send them a review request from their profile. See [Request Strategy](../request-strategy.md) for how requests are triggered.
{% endhint %}

---

### Customer Messages Section

On a customer's profile, the **Messages** section shows every message sent to that customer. If they have messages, you can switch between two views:

* **Grouped by request** – Messages are grouped by review request. Each group shows "Request #1", "Request #2", and so on, with the messages for that request listed below.
* **List** – A flat list of all messages in one table.

If the customer has no messages yet, you'll see a notice: *Request a review to schedule messages.* Send a manual request from the customer's page to get started.

#### Per-Message Actions

Each message row has an **Actions** menu. What you can do depends on the message status:

* **Cancel message** – For unsent messages only. Stops the message from being sent. You can optionally cancel all unsent messages in that request.
* **Reschedule message** – For canceled messages only. Pick a new date and time to send it.
* **Copy UUID** – Copy the message identifier to your clipboard.
* **Delete message** – Remove the message from the list. This does not undo a sent message; it only removes the record from your view.

{% hint style="warning" %}
Deleting a message is permanent. Use cancel or reschedule if you want to change when a message goes out instead.
{% endhint %}

---

### Message Statuses

| Status | Meaning |
|--------|---------|
| **Scheduled** | The message is queued and will be sent at the scheduled time. |
| **Sent** | The message was delivered. |
| **Opened** | The customer opened the email (email only). |
| **Clicked** | The customer clicked the link to leave a review. |
| **Failed** | The message could not be delivered. A reason may be shown. |
| **Complained** | The customer marked the message as spam or complained. |

---

### Tips

{% hint style="info" %}
Use the **Clicked** stat and filter to see which messages led to reviews. These are your most effective messages.
{% endhint %}

{% hint style="success" %}
If a message failed, check the failure reason. Common causes include invalid email addresses, unsubscribed customers, or SMS delivery issues. Fix the underlying issue (e.g., update the customer's contact info) before resending.
{% endhint %}
