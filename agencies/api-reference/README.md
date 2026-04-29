---
description: >-
  White-label Agency API - secret-key automation, live reference, and workflows
  for reviews, ratings, feedback, and reputation.
icon: rectangle-terminal
---

# API Reference

If you run a white-label [reviews and reputation](../white-label.md) business for clients, you can connect your own tools and workflows to your agency account. We call that connection the **Agency API**. It is for teams who already use the console every day and want to **automate agency-wide setup**—so adding businesses, aligning access, and keeping the client experience consistent does not all have to be done by hand.

Think of it as a secure bridge between your systems and your agency space in the product. Each **project** under your agency still represents one customer business you manage—for **review requests**, **ratings**, **feedback**, **reputation** programs, and everything else those clients do in the console. The connection does not replace the console; it helps you scale how you onboard people and tune what they are allowed to see.

Your agency has its own **secret key**. That key lets trusted automation act on behalf of your whole agency—across every customer business you host—not just a single location. It is similar in spirit to the secret key inside a single project’s settings, described in our [project automation reference](../../platform/api-reference/), except the agency key applies to the entire agency.

## The live reference on this page

Below this introduction, the same page includes an **interactive reference** that lists what the Agency API can do today: the operations you can perform, how to authenticate, and the shape of each request and response.

{% hint style="info" %}
That reference is generated from our specification and is updated as we expand or adjust the Agency API. Rely on it for the current, authoritative picture as details may change from time to time.
{% endhint %}

## What this connection is generally for

Typical uses include **provisioning and managing the businesses** you host under your agency, **controlling who is invited** and **what each person can open** in the console, and **keeping agency-level shortcuts and configuration** aligned with your own tools or processes. The exact actions available at any moment are spelled out in the interactive reference on this page—not duplicated here—so the documentation stays accurate as we ship improvements.

{% hint style="info" %}
This is separate from the secret key inside a single project’s settings. The project key only affects that one business. The agency key affects every project under your agency.
{% endhint %}

## Where to find it in the console

1. Open your account and use the **Agency** entry in the header (when your plan includes an agency).
2. In the agency sidebar, open **API**.
3. You will see the **API key** section with your **secret key** and a control that copies it to your clipboard.

If you do not see **API**, or the section is locked and asks you to upgrade, your current plan may not include this kind of automation for agencies. Upgrade or contact support as directed on screen.

{% hint style="success" %}
The **View documentation** button on that screen opens the [White label](../white-label.md) guide—helpful context for domains, branding, and what your clients see.
{% endhint %}

## How to obtain and copy your agency secret key

You do **not** need to create the key yourself. When your agency is created, a secret key is already assigned. To obtain it:

1. Go to **Agency** → **API** as above.
2. Find **Secret key** on the page.
3. Use the copy control so you can paste it only where it belongs (for example, into your own secure automation tool or a password manager your team uses).

Only people who are allowed to view the agency can open this screen. Rotating the key requires permission to change agency settings.

{% hint style="warning" %}
Treat the secret key like a password. Anyone who has it can perform the actions the connection allows across your agency. Do not paste it into shared chat, email, or tickets.
{% endhint %}

## Rotating the key (Change)

If a key might have been exposed, you offboard a vendor, or you want a fresh secret:

1. On **Agency** → **API**, choose **Change**.
2. Read the confirmation: rotating the key immediately invalidates the previous secret. Anything still using the old value will stop working until you update it.
3. Choose **Save** to confirm. The page shows your new secret key—copy it and update every place that stored the old one.

{% hint style="warning" %}
Plan a moment to update every place that stored the old key. Until you do, anything tied to the old secret will fail.
{% endhint %}

## Related documentation

* [White label overview](../white-label.md) — agency setup, domains, and client experience.
* [Project automation reference](../../platform/api-reference/) — secret-key sign-in and actions scoped to a **single** project (customers, review requests, reviews, locations, and more).
