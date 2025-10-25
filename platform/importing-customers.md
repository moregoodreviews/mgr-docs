---
icon: file-import
---

# Importing Customers

In order for MGR to request reviews from your customers, we need to import some data:

#### Customer Data

1. Name - The customer's name.
2. Email - The customer's email address.
3. Phone - The customer's phone number.
4. Company - The customer's company name.
5. Signup Date - The date the customer signed up to your service.

We need this data to send messages, but why the signup date? In your request strategy, you can set how many minutes, hours, or days to wait to send a message after the customer signs up. Think of it as a trigger date. It is the date used to ultimately trigger the sending of messages to a customer.

#### Charge History (Optional)

1. Charge Date - When the customer was charged.
2. Charge Amount - How much the customer was charged.
3. Subscription Info - Whether or not the customer has a subscription.

We automatically save charge history if you connect a Stripe account, but you can also send it in via an app connector or our REST API. Why do we need charge history? You can tailor your request strategy to only request reviews from customers who have made at least 3 charges, for example. Or spent at least $100, or have an average charge of $20, or have an active subscription. This helps you better target customers who are likely to leave positive reviews.

## Import Options

### Stripe

Automatically import your Stripe customers with charge history. Perfect for requesting reviews from  paying customers or customers on a subscription.

### HubSpot

Automatically import your HubSpot contacts. You can choose which contacts to import by their lifecycle stage, or sync them all.

### App Connector

We have integrations with: [Zapier](https://zapier.com/apps/more-good-reviews/integrations), [Pabbly](https://accounts.pabbly.com/login/?s=connect\&pl=https://connect.pabbly.com/share-app/CUFRYwBlVTdTGARADkEHYltIBzACXlNpVUVUXQFkB0EHKAlBBmwKFQx3U0UHf1VmAG0), [Make](https://www.make.com/en/hq/app-invitation/0b3a8c3446b8c2f7cfc1acdcf434104c), [Boost.space](https://integrator.boost.space/app/invite/096ef2f6f3a68a7099ad125c107a69cf)

Send customer data into MGR from thousands of 3rd party apps and CRMs with an app connector. If you are not familiar with using APIs, this solution is perfect for you, and it will allow to work with just about any service to get your customer data into the platform.

### Email BCC

Each project has a specific BCC email. Use this email in the BCC field when sending receipts or invoices to customers. This automatically imports their name and email address. This option will not be available if you use your SMTP credentials for sending emails.

### REST API

Send customer data from your server with our simple REST API. We offer endpoints for importing customers and charges. Check out our [API Reference](api-reference.md).

### CSV Upload

You can upload a CSV file to import thousands of customer records at once. It is a convenient way to get started quickly. We accept the following values:

| Header         | Value                                                                                           |
| -------------- | ----------------------------------------------------------------------------------------------- |
| first\_name\*  | The customer’s first name.                                                                      |
| last\_name     | The customer’s last name.                                                                       |
| email          | The customer’s email address.                                                                   |
| phone          | The customer’s phone number.                                                                    |
| company        | The customer’s company name.                                                                    |
| location       | The slug or UUID of a [location](https://www.moregoodreviews.test.com:8090/settings/locations). |
| signed\_up\_at | The customer’s start date. YYYY-MM-DD                                                           |

{% hint style="info" %}
Download an example CSV template, [here](https://moregoodreviews.com/csv/customers.csv).
{% endhint %}

### Manual Entry

You can manually enter customer data directly in our app. While it is not an automated solution, it is a simple way to get started. Just click the Import button on the [Customers](https://moregoodreviews.com/customers?import=1) page.

### Suggest an Integration

Have an idea for an integration? [Let us know](http://feedback.moregoodreviews.com) and we can build it for you!

