---
description: >-
  Introduction to the Agency API for white-label agencies: what the connection
  is for, agency secret key (find, copy, rotate), clients and projects,
  reviews, ratings, feedback, and reputation at scale—plus the interactive
  reference on this page.
icon: rectangle-terminal
---

# API Reference (Beta)

If you run a white-label [reviews and reputation](../white-label.md) business for clients, you can connect your own tools and workflows to your agency account. We call that connection the **Agency API**. It is for teams who already use the console day to day but also want to **provision clients**, **align access**, and **keep sidebar shortcuts in sync** without doing every step by hand.

Think of it as a secure bridge between your systems and your agency space in the product. Each **project** under your agency still represents one customer business you manage—not only for **review requests**, **ratings**, **feedback**, and **reputation** work, but for everything else those clients do in the console. The connection does not replace the console; it helps you scale how you set things up and who can see what.

Your agency has its own **secret key**. That key lets trusted automation work across your entire agency—every customer business you host—not just one location. It works like the secret key inside a single project’s settings, described in our [project automation reference](../../platform/api-reference.md), except yours applies to the whole agency.

Use the interactive reference linked in the sidebar under this page for the full list of what you can do and the details behind each action. The sections below explain what the key is for, where to find it in the console, and how to keep it safe—so your team knows what clients will experience when you manage **review requests**, **ratings**, **feedback**, and **reputation** at scale.

## What this connection is for

With the agency secret key, automation can:

* Create and list **projects** (each project is one client business you manage under the agency).
* **Suspend** or **restore** a project, or **remove** one when a client leaves—so access and sending line up with your agreements.
* **See everyone in your client list**—people you have invited and people who have already joined—including which businesses each person can open and which parts of the console they may use.
* **Invite clients** by email, choose their role, decide which projects they see, and limit which areas they can open (for example **reviews**, **ratings**, **messages**, analytics, or other sections you allow).
* Look up the **names and identifiers of console areas** your product supports, so invitations and reporting stay consistent when you grant access.
* Add, change, or remove **external links** that appear in your clients’ sidebar—handy for booking pages, your site, or other tools.

Together, this keeps day-to-day work organized as you add clients and tune what each person is allowed to see.

{% hint style="info" %}
This is separate from the secret key inside a single project’s settings. The project key only affects that one business. The agency key affects every project under your agency.
{% endhint %}

{% hint style="warning" %}
If an address already has a **pending** invitation, sending another invite to that same address will not succeed until the pending invite is resolved or the person finishes creating their account. Check your client list before retrying.
{% endhint %}

## Where to find it in the console

1. Open your account and use the **Agency** entry in the header (when your plan includes an agency).
2. In the agency sidebar, open **API**.
3. You will see the **API key** section with your **secret key** and a control that copies it to your clipboard.

If you do not see **API**, or the section is locked and asks you to upgrade, your current plan may not include this kind of automation for agencies. Upgrade or contact support as directed on screen.

{% hint style="success" %}
The View documentation button on that screen opens the [White label](../white-label.md) guide—helpful context for domains, branding, and what your clients see.
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
* [Project automation reference](../../platform/api-reference.md) — secret-key sign-in and actions scoped to a **single** project (customers, review requests, reviews, locations, and more).
