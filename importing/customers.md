---
description: >-
  Bring your customers into MGR so you can request reviews. Import via CSV,
  integrations, BCC, manual entry, or the REST API.
icon: file-import
---

# Customers

To request reviews from your customers, you need to bring them into MGR first. This page explains what data you need, where to find the import options, and how each method works.

### Where to Import

Go to **Customers** in the sidebar and click **Add**. A modal opens with tabs for each import method: **Manual Entry**, **Upload CSV**, **Integrations**, and **BCC** (if available). You can also open a specific tab directly—for example, add `?import=csv` to the Customers page URL to open the CSV tab.

***

### What Data You Need

#### Required for Sending Messages

You need at least one way to reach each customer:

* **Email** – For sending review requests and reminders by email.
* **Phone** – For sending review requests and reminders by SMS. Use a full number with country code (e.g., +18888888888).

Without an email or phone number, MGR cannot send messages to that customer.

#### Customer Data

| Field           | Purpose                                                          |
| --------------- | ---------------------------------------------------------------- |
| **Name**        | First and last name. Used in messages and to identify customers. |
| **Email**       | Required for email requests.                                     |
| **Phone**       | Required for SMS requests.                                       |
| **Company**     | Optional. Shown on customer profiles.                            |
| **Signup Date** | The date that triggers your request strategy. See below.         |

#### Why the Signup Date Matters

Your [Request Strategy](../platform/request-strategy.md) decides when to send the first review request. You can set a delay such as "14 days after signup" or "2 hours after charge." The **signup date** is the date used when the trigger is "send after a date." Think of it as the start date for that customer—when they joined, paid, or completed a purchase. If you leave it blank, today's date is used.

#### Charge History (Optional)

If you connect Stripe, charge history is imported automatically. You can also send it via an app connector or the REST API. Charge history lets you target customers in your request strategy—for example, only request reviews from customers who have made at least 3 charges, spent $100 or more, or have an active subscription. This helps you focus on customers who are more likely to leave positive reviews.

***

### Import Methods

#### Manual Entry

Add one customer at a time. Fill in their name, email, phone, company, location (if you use locations), tags, and signup date. You can optionally schedule a review request immediately and choose the channel (email or SMS), reminders, and review page.

{% hint style="info" %}
Manual entry is ideal when you have a few customers or want to add someone quickly. For larger lists, use CSV or an integration.
{% endhint %}

#### CSV Upload

Upload a CSV file to import up to 1,000 customers at once. The import runs in the background; you'll see a confirmation when it's scheduled. Customers appear in your list shortly after.

**Steps:**

1. Go to **Customers** and click **Add**.
2. Open the **Upload CSV** tab.
3. Click **Download Template** to get a sample file with the correct headers.
4. Fill in your data and save as CSV (UTF-8).
5. Click **Upload CSV** and select your file.

**CSV Headers**

| Header         | Required | Description                                                                              |
| -------------- | -------- | ---------------------------------------------------------------------------------------- |
| first\_name    | Yes      | The customer's first name.                                                               |
| last\_name     | No       | The customer's last name.                                                                |
| email          | No       | The customer's email address.                                                            |
| phone          | No       | The customer's phone number.                                                             |
| company        | No       | The customer's company name.                                                             |
| location       | No       | The slug or UUID of a location. Must match a location in **Settings > Locations**.       |
| notes          | No       | Internal notes (not shown to customers).                                                 |
| tags           | No       | Comma-separated list of tag slugs. Tags must exist in your project and be for customers. |
| signed\_up\_at | No       | The customer's start date. Use YYYY-MM-DD format.                                        |
| unsubscribed\_at | No     | The date the customer unsubscribed, if any. Use YYYY-MM-DD format. Leave blank for subscribed customers. |
| address1       | No       | Address line 1.                                                                          |
| address2       | No       | Address line 2.                                                                          |
| city           | No       | City or locality.                                                                        |
| state          | No       | State or region.                                                                         |
| postal\_code   | No       | Postal or ZIP code.                                                                      |

{% hint style="warning" %}
Each row must have either an email or a phone number. Duplicate emails or phones in your project will update the existing customer instead of creating a new one.
{% endhint %}

{% hint style="info" %}
Download an example CSV template from [moregoodreviews.com/csv/customers.csv](https://moregoodreviews.com/csv/customers.csv).
{% endhint %}

{% hint style="success" %}
Migrating from another review platform? Add an `unsubscribed_at` column to your CSV with the date each customer opted out. MGR will skip review requests for those customers and respect their unsubscribed status.
{% endhint %}

#### Stripe

Connect your Stripe account to automatically import customers and their charge history. Ideal if you want to request reviews from paying customers or subscribers. Set up the connection under **Settings > Integrations**.

Refunds are handled automatically. When a charge is refunded in Stripe, MGR records a matching negative charge so the customer's net spend stays accurate. This means request strategies that filter by spend won't keep targeting customers who got their money back.

#### HubSpot

Connect HubSpot to import contacts. You can choose which contacts to import by lifecycle stage or sync them all. Set up under **Settings > Integrations**.

#### App Connectors (Zapier, Make, Pabbly, Boost.space)

Use an app connector to send customer data from thousands of apps and CRMs into MGR. No coding required. Useful if your CRM or tool isn't natively supported. Set up under **Settings > Integrations**.

Connectors: [Zapier](https://zapier.com/apps/more-good-reviews/integrations), [Pabbly Connect](https://accounts.pabbly.com/login/?s=connect\&pl=https://connect.pabbly.com/share-app/CUFRYwBlVTdTGARADkEHYltIBzACXlNpVUVUXQFkB0EHKAlBBmwKFQx3U0UHf1VmAG0), [Make](https://www.make.com/en/hq/app-invitation/0b3a8c3446b8c2f7cfc1acdcf434104c), [Boost.space](https://integrator.boost.space/app/invite/096ef2f6f3a68a7099ad125c107a69cf).

#### Email BCC

Each project has a unique BCC email address. When you send receipts, invoices, or other emails to customers, add this address in the BCC field. MGR will import the recipient's name and email from each email automatically.

**How to use it:**

1. Go to **Customers** and click **Add**.
2. Open the **BCC** tab.
3. Copy the BCC email address shown.
4. Add it to the BCC field in your email system when sending to customers.

{% hint style="warning" %}
The BCC option is only available when your project uses the platform's email delivery (not your own SMTP). If you send via your own SMTP server, BCC import may not work.
{% endhint %}

{% hint style="info" %}
BCC is great for businesses that already email customers (e.g., receipts or invoices). Each time you send, new customers are imported without extra steps.
{% endhint %}

#### REST API

Send customer data from your own server using the REST API. Endpoints are available for importing customers and charges. See the [API Reference](../platform/api-reference/) for details.

***

### After Import

* **CSV imports** – The import runs in the background. You may receive an email when it completes. Customers appear on the Customers page as they are processed.
* **Integrations** – Stripe and HubSpot sync continuously. New and updated customers are imported automatically.
* **BCC** – Each BCC'd email creates or updates a customer as soon as the email is received.
* **Manual entry** – The customer appears immediately.

Once customers are in your project, configure your [Request Strategy](../platform/request-strategy.md) and turn on automatic review collection to start requesting reviews. You can also send manual review requests from individual customer profiles.

***

### Tips

{% hint style="success" %}
Use the signup date to control when each customer gets their first request. For example, set it to the date they made a purchase so your "7 days after signup" delay sends the request 7 days after that purchase.
{% endhint %}

{% hint style="info" %}
If you have multiple locations, include the `location` column in your CSV with the correct slug or UUID. Customers will be assigned to that location for filtering and reporting.
{% endhint %}

{% hint style="info" %}
Tags in the CSV must use tag slugs (the URL-friendly name) and must already exist in your project under Settings > Tags. Use comma-separated values for multiple tags.
{% endhint %}

### Suggest an Integration

Have an idea for a native integration? [Let us know](http://feedback.moregoodreviews.com) and we can build it for you.
