---
icon: message
---

# SMS with ClickSend

### Getting Started

In order to send review requests over SMS, you can use your own ClickSend account. You can register [here](https://www.clicksend.com/), if you do not already have one. You will need to:

1. Locate your API key and username (email address) in Developers > API Credentials
2. Locate your user ID in the header of the console
3. Buy and register a phone number if you are sending in US or Canada

ClickSend uses a shared number if you are sending outside of US and Canada, so it may not be necessary for you to purchase one. You can also add multiple numbers to your account, and ClickSend will automatically use the best number for the customer you are sending the SMS to.

### Integration with MGR

Once you have created your ClickSend account, you can integrate it with MGR and start sending messages right away. To establish the connection, go to your project integrations and click on the [ClickSend integration](https://moregoodreviews.com/settings/integrations/clicksend). Add:

* Your user ID
* Your username (email address)
* Your API key

Your ClickSend user ID is located in the header of the console in the profile dropdown menu. Your username and API key can be found in Developers > API Credentials.

### Webhook for Delivery Status & Unsubscribing

In order for MGR to know if a message was delivered, as well as listen for the STOP keyword to unsubscribe, you will need to add a new [Inbound Rule](https://dashboard.clicksend.com/messaging-settings/sms/inbound-sms) and [Delivery Report Rule](https://dashboard.clicksend.com/messaging-settings/sms/delivery-reports) on ClickSend. The URL for each rule is provided to you when integrating ClickSend with MGR on the integration page. The rules can be found in the Messaging Settings section, which you can access from the profile dropdown in the header of the console.

#### Inbound Rule

Create a new rule for any number and any message, and set the action to URL. Enter the Incoming Webhook URL provided to you on the MGR integration page, and save the rule.

#### Delivery Report URL

Create new rule to match all reports, and set the action to URL. Enter the Incoming Webhook URL provided to you on the MGR integration page, and save the rule.
