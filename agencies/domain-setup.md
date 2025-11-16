---
description: This step is essential to white label the platform.
icon: cloud
---

# Domain Setup

To white label the software, you will need to configure your own domain to send emails and also run the website at your own web address. Therefore the domain setup is the most critical component of white labeling.

We offer the following options for the domain configuration:

* Sending Domain - Used to send system emails to your clients, like platform notifications, user invites, and reports. It is also used for sending emails on your clients' behalf to their customers, unless a sending domain is added to each of your clients' projects. You should add a sending domain to every project, so your clients can send emails from their own domain, and not your agency sending domain.
* Client Portal Domain - Used for the portal your clients will sign into. It also acts as a fallback domain for the review pages and showcases of your clients' customers, if your client does not add their own.
* Widget Tag Domain - Used in the embed code for widgets. The domain will be exposed to your clients, so you can optionally add this if you plan to offer widgets.
* Image URL Domain - Used for any images uploaded to the platform. Your clients may only see this domain if they inspect a page an image is loaded on.
* API Domain - You may optionally white label our API if you plan to offer that to your clients.

### Sending Domain Setup

You will need to enter 4 DNS records to set up your sending domain. 2 TXT records and 2 MX records. This allows us to send emails on your behalf. We use a service called [Mailgun](https://www.mailgun.com/) to do this.

{% hint style="danger" %}
If you do not add your own sending domain, all platform emails sent to your clients will come from notifications@moregoodreviews.com.
{% endhint %}

### CNAME Setup

Any domain that is not a sending domain is considered a CNAME. This means it is simply a subdomain you set up in your DNS that points to our platform. You will need to add 1 CNAME record and 1 TXT record per CNAME. After adding your domain in the console, a TXT record will be generated within a few minutes. This TXT record is required for SSL certificate issuance, enabling us to serve your assets securely over HTTPS.

{% hint style="danger" %}
If you do not add the CNAME for the client portal, the software will not be white labeled, and your clients will be directed to moregoodreviews.com to create an account.
{% endhint %}

