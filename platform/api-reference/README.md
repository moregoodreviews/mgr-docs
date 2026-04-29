---
description: >-
  Project API - secret-key automation, live reference, and workflows for
  reviews, ratings, feedback, customers, and reputation.
icon: rectangle-terminal
---

# API Reference

If you manage customer reviews, ratings, feedback, and reputation work inside a project, you can connect your own tools and workflows to that project. We call that connection the **Project API**. It is for teams who already use the console and want to **automate project-level work** without doing every customer, review request, location, or tag update by hand.

Think of it as a secure bridge between your systems and one project in the product. The connection does not replace the console; it helps you keep customer records, review requests, reviews, ratings, messages, locations, sources, and tags aligned with the tools your team already uses.

Your project has its own **secret key**. That key lets trusted automation act on behalf of that project only. It is similar in spirit to the agency secret key described in our [Agency API reference](../../agencies/api-reference/), except the project key is limited to one project instead of every business under an agency.

## The live reference on this page

Below this introduction, the same page includes an **interactive reference** that lists what the Project API can do today: the operations you can perform, how to authenticate, and the shape of each request and response.

{% hint style="info" %}
That reference is generated from our specification and is updated as we expand or adjust the Project API. Rely on it for the current, authoritative picture as details may change from time to time.
{% endhint %}

## What this connection is generally for

Typical uses include **importing and updating customers**, **recording customer activity**, **sending review requests**, **reviewing feedback and ratings**, **organizing locations, sources, and tags**, and **syncing reputation data** into your own reporting or customer tools. The exact actions available at any moment are spelled out in the interactive reference on this page, not duplicated here, so the documentation stays accurate as we ship improvements.

{% hint style="info" %}
This is separate from the agency key. A project key only affects the project where you copied it. An agency key can affect multiple projects under the agency.
{% endhint %}

## Where to find it in the console

1. Open the project you want to connect.
2. Go to **Settings** in the sidebar.
3. Open **API**.
4. You will see the **API key** section with your **secret key** and a control that copies it to your clipboard.

If you do not see **API**, or the section is locked and asks you to upgrade, your current plan may not include project automation. Upgrade or contact support as directed on screen.

{% hint style="success" %}
The **View documentation** button on that screen opens this reference page.
{% endhint %}

## How to obtain and copy your project secret key

You do **not** need to create the key yourself. When your project is created, a secret key is already assigned. To obtain it:

1. Go to **Settings** > **API** as above.
2. Find **Secret key** on the page.
3. Use the copy control so you can paste it only where it belongs (for example, into your own secure automation tool or a password manager your team uses).

Only people who are allowed to manage the project can open this screen. Rotating the key requires permission to change project settings.

{% hint style="warning" %}
Treat the secret key like a password. Anyone who has it can perform the actions the connection allows inside that project. Do not paste it into shared chat, email, or tickets.
{% endhint %}

## Rotating the key (Change)

If a key might have been exposed, you offboard a vendor, or you want a fresh secret:

1. On **Settings** > **API**, choose **Change**.
2. Read the confirmation: rotating the key immediately invalidates the previous secret. Anything still using the old value will stop working until you update it.
3. Choose **Save** to confirm. The page shows your new secret key. Copy it and update every place that stored the old one.

{% hint style="warning" %}
Plan a moment to update every place that stored the old key. Until you do, anything tied to the old secret will fail.
{% endhint %}

## Webhooks

The same **Settings** > **API** area also includes **Webhooks** when your plan includes them. Webhooks let your project send updates to another tool when supported activity happens, so your team can keep review, feedback, customer, and reputation workflows in sync.

## Related documentation

* [Projects](../projects.md) - project setup and the main project workspace.
* [Customers](../projects/customers.md) - customer records used for review requests and feedback.
* [Reviews](../projects/reviews.md) - customer reviews, ratings, and reputation tracking.
* [Agency API reference](../../agencies/api-reference/) - secret-key automation scoped to an **agency** instead of one project.
