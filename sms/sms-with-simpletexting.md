---
icon: message
---

# SMS with SimpleTexting

## Getting Started

In order to send review requests over SMS, you can use your own SimpleTexting account. You can register [here](https://www.simpletexting.com/), if you do not already have one. You will need to:

1. Activate a phone number
2. Register your number to be in compliance&#x20;
3. Request API access in Integrations > API & Webhooks

All of these steps can be done in a single day. You can read about the steps to [registering a number](https://help.simpletexting.com/en/articles/4729632-how-to-register-your-local-number-with-simpletexting) with SimpleTexting and [requesting API access](https://help.simpletexting.com/en/articles/1040620-can-i-try-your-api) on their Help Center. SimpleTexting is known for a quick and speedy registration process compared to other SMS providers.

## Integration with MGR

Once you have your activated phone number and your API token, you are ready to connect your account to MGR to request reviews over SMS. To establish the connection, go to your project integrations and click on the [SimpleTexting integration](https://moregoodreviews.com/settings/integrations/simpletexting). Add:

* Your phone number (digits only)
* Your API token

This is all that is needed to set up SMS with SimpleTexting on our end. If your credentials are correct, and your account has an activated and registered number, you are just about done.

{% hint style="info" %}
You may need to reach out to SImpleTexting support to increase customer and inbox limits on their end. If you are seeing failed messages in MGR, this is likely the cause.
{% endhint %}

## Webhook for Delivery Status & Unsubscribing

In order for MGR to know if a message was delivered, as well as listen for the STOP keyword to unsubscribe, you will need to add a new subscription in the [Webhooks](https://app2.simpletexting.com/integrations/webhooks) section on SimpleTexting. This URL is provided to you when integrating SimpleTexting with MGR on the integration page.

Copy the Incoming Webhook URL from MGR and then paste that into the field for Target URL when creating a new webhook subscription.  For triggers, select:

* Incoming Message
* Outgoing Message
* Delivery Report
* Non-Delivered Report
* Unsubscribe Report

Do this for "All Messages" and save the webhook subscription.
