---
description: >-
  Use a dedicated agency API key for integrations that operate across your
  agency, separate from each project's API key.
icon: key
---

# API (Agency Settings)

Agencies can use a **secret API key** scoped to the agency, in the same way each project has its own API key. Use it to authenticate requests against agency-level API endpoints when those endpoints are available in your plan.

### Where to Find It

Open **Agency** in the header, then go to **Settings** and open the **API** page.

### API Key Section

The **API Key** section works like the API key on project settings:

* **Copy** – Copy the key to use in your integration or scripts.
* **Change key** – Generate a new key. After you change it, the old key stops working immediately. Update any systems that still use the old key.

{% hint style="warning" %}
Treat your agency API key like a password. Anyone with the key can act on behalf of your agency within the API's scope. Do not commit it to source control or share it in public channels.
{% endhint %}

### How This Relates to Project Keys

* Each **project** under your account still has its own API key (see [API Reference](../platform/api-reference.md)). Use a **project** key for endpoints that target a single project (for example, customers, reviews, and locations for that project).
* Use the **agency** key only for endpoints that are explicitly designed for agency-wide operations. The product will document which key to use for each endpoint.

### Rolling Out Keys for Existing Agencies

If your agency was created before agency API keys existed, a one-time migration ensures every agency receives a key. You do not need to do anything unless you are told otherwise; open **Agency > Settings > API** to view or rotate your key.
