---
description: Connect your tools to collect reviews, send requests, and get notified when customers leave feedback.
icon: plug
---

# Integrations

Integrations connect More Good Reviews with the tools you already use. **Google My Business is the most important**—it lets you sync and reply to Google reviews from MGR. You can also sync reviews from Facebook, send review requests to customers in Stripe or HubSpot, get instant alerts in Slack or Discord when new reviews arrive, and request reviews over SMS. Application connectors like Zapier and Pabbly let you build custom workflows with your reviews and customer data.

### Where to Find Integrations

Go to **Settings** in the sidebar and click **Integrations**. You’ll see all available integrations grouped by type: Reviews, CRMs, Notifications, and SMS. Click any integration to connect it to your project.

---

## Review Integrations

These integrations bring reviews into your project from external sites. Once connected, reviews sync automatically so you can manage them in one place.

### Google My Business

Google My Business is the most important integration for most businesses. Sync your Google business reviews into MGR. When you connect Google My Business, you choose which business locations to sync. Reviews from those locations are imported and kept up to date. You can also reply to Google reviews directly from MGR.

{% hint style="info" %}
Google My Business supports multiple locations. After connecting, select the locations you want to sync. Reviews from unselected locations will not be imported.
{% endhint %}

---

## CRM Integrations

CRM integrations let you send review requests to customers stored in your existing tools. When you connect Stripe or HubSpot, MGR can pull in your customers and send them review request messages at the right time.

### Stripe

Send review requests to your Stripe customers. Connect your Stripe account and MGR will sync your customer list. You can then send review requests by email or SMS to customers after a purchase or charge. This helps you collect feedback and build your reputation right when the experience is fresh.

### HubSpot

Send review requests to your HubSpot contacts. Connect your HubSpot account and MGR will sync your contacts. You can send review requests by email or SMS based on your contact list and workflow. Use this to gather reviews and ratings from leads and customers in your CRM.

{% hint style="success" %}
CRM integrations work best when paired with a [Request Strategy](request-strategy.md). Set rules for when to send review requests—for example, after a successful charge or when a contact reaches a certain stage.
{% endhint %}

---

## Alert Integrations

Alert integrations notify your team when customers leave reviews. New reviews are sent to your Slack channel or Discord server so you can respond quickly and stay on top of feedback.

### Slack

Get notified in Slack when customers review your business. Connect your Slack workspace and choose the channel where you want review notifications to appear. Each new review triggers a message in that channel with the customer’s rating, feedback, and a link to reply.

### Discord

Get notified in Discord when customers review your business. Connect your Discord server and add the MGR bot. New reviews are posted to the channel you select, so your team can see feedback as it comes in and respond from MGR.

---

## SMS Integrations

SMS integrations let you request reviews from customers over text message. You connect your own Twilio, ClickSend, or SimpleTexting account and provide your credentials. MGR then sends review request links via SMS as part of your message strategy.

### Twilio

Request reviews from your customers over SMS using Twilio. You’ll need a Twilio account, a phone number, and a messaging service. Add your account credentials in the Twilio integration page. MGR provides a webhook URL to paste into Twilio so delivery status and STOP/unsubscribe requests are handled correctly.

For setup details, see [SMS with Twilio](../sms/sms-with-twilio.md).

### ClickSend

Request reviews from your customers over SMS using ClickSend. Connect your ClickSend account by adding your credentials in the integration page. MGR will use your account to send review request links when your message strategy triggers an SMS.

For setup details, see [SMS with ClickSend](../sms/sms-with-clicksend.md).

### SimpleTexting

Request reviews from your customers over SMS using SimpleTexting. Connect your SimpleTexting account by adding your credentials in the integration page. MGR will use your account to send review request links when your message strategy triggers an SMS.

For setup details, see [SMS with SimpleTexting](../sms/sms-with-simpletexting.md).

---

## Application Connectors

Application connectors let you build custom workflows with your reviews and customer data. Zapier, Pabbly, Make, and Boost Space can trigger actions when reviews are created, when messages are sent, or when other events occur in your project.

### Zapier

Connect MGR to thousands of apps through Zapier. Create Zaps that run when a new review arrives, when a message is sent, or when other events happen. For example, add new reviewers to a spreadsheet, post reviews to social media, or update your CRM when feedback comes in.

### Pabbly

Connect MGR to other tools using Pabbly. Build workflows that run when reviews or messages are created or updated. Use Pabbly to automate how you use your review data across your other systems.

### Make

Connect MGR to Make (formerly Integromat) to automate workflows. Trigger scenarios when reviews or messages are created, and connect to hundreds of apps for custom automation.

### Boost Space

Connect MGR to Boost Space to build automation workflows. Use your review and message data to trigger actions in other tools and keep your systems in sync.

{% hint style="info" %}
Application connectors typically use webhooks or the MGR app in their marketplace. For more control, you can also add [Webhooks](projects/webhooks.md) in Settings > API to send events to any URL you choose.
{% endhint %}

---

## Webhooks and API

Beyond the integrations above, you can connect MGR to any system using webhooks or the API.

### Webhooks

Webhooks send events to a URL you provide when something happens—for example, when a review is created or updated, or when a message is sent. Add webhook URLs in **Settings > API** under the Webhooks section. This is useful for custom dashboards, internal tools, or connecting to systems that aren’t in the integration list.

For details, see [Webhooks](projects/webhooks.md).

### API

Use the MGR API to import customers, send review requests, export reviews, and more. Your project has an API key in **Settings > API**. The API is ideal for developers who want to build custom integrations or automate workflows programmatically.

For details, see [API Reference](api-reference.md).

---

## Connecting and Disconnecting

**To connect an integration:** Go to Settings > Integrations, click the integration you want, and click **Connect**. You’ll be redirected to sign in or authorize the connection. After you approve, you’re brought back to MGR and the integration is active.

**To disconnect:** Open the integration page and click **Disconnect** at the bottom. Your existing data (reviews, messages) remains in MGR, but no new data will sync and no new messages will be sent through that integration.

**To resync:** Some integrations (like Google My Business, Stripe, and HubSpot) support syncing. If you’ve connected and want to pull in the latest data, click **Sync** or **Resync** on the integration page. Syncing runs in the background; you may see a status update when it completes.

---

## Tips

{% hint style="success" %}
Combine multiple integrations for the best results. For example, sync reviews from Google, send requests to Stripe customers, and get Slack alerts when new feedback arrives.
{% endhint %}

{% hint style="info" %}
If you have multiple locations, connect Google My Business and select which locations to sync. Reviews will be tagged by location so you can filter and report by store or branch.
{% endhint %}

{% hint style="warning" %}
SMS integrations require your own Twilio, ClickSend, or SimpleTexting account. You’ll need to register a phone number and set up your messaging service before connecting to MGR.
{% endhint %}
