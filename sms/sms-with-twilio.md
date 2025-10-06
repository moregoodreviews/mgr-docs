---
icon: message
---

# SMS with Twilio

## Getting Started

In order to send review requests over SMS, you can use your own Twilio account. You can register [here](https://www.twilio.com/), if you do not already have one. You will need to:

1. Register a phone number
2. Add the number to a messaging service
3. Register a campaign for your messaging service to be in compliance

For help from Twilio on getting started with your account, you can read [Milestones For Onboarding your SMS Project to Twilio](https://www.twilio.com/en-us/blog/insights/best-practices/milestones-onboarding-your-sms-project-to-twilio).

## Integration with MGR

When you create a new messaging service, you'll get an SID (string identifier) for it. You'll need this, along with your account SID and auth token to connect the service to MGR. To establish the connection, go to your project integrations and click on the [Twilio integration](https://moregoodreviews.com/settings/integrations/twilio). Add:

1. Your account [auth token](https://help.twilio.com/articles/223136027-Auth-Tokens-and-How-to-Change-Them)
2. Your account SID
3. Your messaging service SID

This is all that is needed to set up SMS with Twilio on our end. If all your credentials are correct, and your account has a working and approved messaging service, you are just about done.

{% hint style="info" %}
If you need help setting up your messaging service on Twilio, [read this guide](https://help.twilio.com/articles/223181308-Getting-started-with-Messaging-Services).
{% endhint %}

## Webhook for Delivery Status & Unsubscribing

In order for MGR to know if a message was delivered, as well as listen for the STOP keyword to unsubscribe, you will need to add a callback URL in your messaging service's settings. This URL is provided to you when integrating Twilio with MGR on the integration page.

Copy the Incoming Webhook URL from MGR and then paste that into the field for Callback URL in the Delivery Status Callback section for your messaging service's integration settings on Twilio.

You should also paste the URL in the field for Send a Webhook > Request URL in the Incoming Messages section. Use POST as the method.

