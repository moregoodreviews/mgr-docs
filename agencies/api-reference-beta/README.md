---
description: >-
  Agency secret key: where to find it, how to copy or rotate it, and an
  interactive reference for projects, clients, and sidebar links across
  your white-label reviews and reputation workspace.
icon: rectangle-terminal
---

# API Reference (Beta)

If you run a white-label [reviews and reputation](../white-label.md) business for clients, your agency has its own **secret key**. That key lets trusted automation work across your entire agency—every customer business you host—not just one location. It works like the secret key inside a single project’s settings, described in our [project automation reference](../../platform/api-reference.md), except yours applies to the whole agency.

Use the interactive reference linked in the sidebar under this page for the complete list of actions and details. The sections that follow explain what the key is for, where to find it in the console, and how to keep it safe.

## What this connection is for

With the agency secret key, automation can:

* Create and list **projects** (each project is one client business you manage).
* **Suspend** or **restore** a project, or **remove** one when a client leaves—so access and sending line up with your agreements.
* **Invite clients** by email, choose their role, decide which projects they see, and limit which parts of the console they can open (such as reviews, ratings, messages, or other sections you allow).
* Add, update, or remove **external links** that appear in your clients’ sidebar—handy for booking pages, your site, or other tools.

Together, this keeps your **review requests**, **feedback**, and **reputation** programs organized as you scale from a handful of clients to many.

{% hint style="info" %}
This is separate from the secret key inside a single project’s settings. The project key only affects that one business. The agency key affects every project under your agency.
{% endhint %}

## Where to find it in the console

1. Open your account and use the **Agency** entry in the header (when your plan includes an agency).
2. In the agency sidebar, open **API**.
3. You will see the **API key** section with your **secret key** and a control that copies it to your clipboard.

If you do not see **API**, or the section asks you to upgrade, your current plan may not include this kind of automation for agencies. Upgrade or contact support as directed on screen.

{% hint style="success" %}
The View documentation action on that screen opens general agency articles (such as white label setup).
{% endhint %}

## How to obtain and copy your agency secret key

You do **not** need to create the key yourself. When your agency is created, a secret key is already assigned. To obtain it:

1. Go to **Agency** → **API** as above.
2. Find **Secret key** on the page.
3. Use the copy control so you can paste it only where it belongs (for example, into your own secure automation tool or a password manager your team uses).

Only people who are allowed to view the agency can open this screen. Rotating the key requires approval to change agency settings.

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
* [Project automation reference](../../platform/api-reference.md) — secret-key sign-in and actions scoped to a **single** project (customers, review requests, reviews, locations, and more).
