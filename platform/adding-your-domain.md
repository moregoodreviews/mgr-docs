---
icon: cloud
---

# Adding Your Domain

### Sending Domain

By default, all emails for a project will be sent from our own domain name. Since it is a shared system, the email address will follow this pattern for each new project:

**reviews+\[PROJECT\_SLUG]@moregoodreviews.net**

You can change the email address by connecting your own domain name to MGR. In the [Domain Settings](https://moregoodreviews.com/settings/domain) section, add a domain that you own in the field. You will need to enter 4 DNS records to set up your sending domain. 2 TXT records and 2 MX records. This allows us to send emails on your behalf. We use a service called [Mailgun](https://www.mailgun.com/) to do this.

MX records are optional but recommended for better deliverability. While we don’t process incoming emails, some providers may mark your messages as spam if the sending domain has no MX records (inbox). Because the sending domain uses a subdomain, this won’t interfere with any inbox set up on your root domain.

Once all records are verified, the system will begin to send emails from your own domain name. If you want to change the left side of the email address and the sender name, you can do that in the [Email Settings](https://moregoodreviews.com/settings/email) section. We recommend using a real person's name as the sender, like "Scott from More Good Reviews".

{% hint style="info" %}
Please note that the domain won’t display a website, so visiting it in your browser won’t load a page. This is expected — the domain is used solely for sending emails.
{% endhint %}

#### DMARC Record

You will also need to add the suggested DMARC record to ensure your emails land in customer inboxes. DMARC is a way to stop fake emails that pretend to be from you. It checks if emails really come from your domain and can tell you when someone tries to fake it, helping keep your emails safe.

### **CNAME - Customer Facing Pages**

Much like the sending domain, all customer facing pages, like your review pages and showcase pages, will be loaded from our own domain: moregoodreviews.com. This means the links in all your messages will have our domain name in them. If you don't mind that, you don't have to do anything. But if you want your links to match your brand, you should add a CNAME record in the [Domain Settings](https://moregoodreviews.com/settings/domain) section.

Note that the example subdomain provided is “review” (singular). After adding your domain, a CNAME record will appear immediately, and a TXT record will show up a few minutes later. You must add both records to your DNS. Once verified, your customer-facing pages will use your own domain.

#### Troubleshooting

1. Have you added both the CNAME and TXT records? The TXT record may take a few minutes to appear after adding your CNAME domain in the console. It’s required for SSL, ensuring your pages load over https. A common issue is the page not loading correctly because the SSL certificate hasn’t been issued yet.
2. If you are using Cloudfare, when entering your CNAME record, it is important your turn OFF the orange proxy switch. We use Cloudflare, and it cannot proxy to itself.
3. If the TXT record isn’t added to your DNS quickly, it may time out and disappear from the console. If that happens, remove the CNAME and add it again to generate a new TXT record for your DNS.

If you are still having trouble getting your CNAME to work, it might mean that Cloudflare cannot validate your SSL certificate. Try adding CAA records to your DNS and re-verifying in MGR. More on this here: [https://developers.cloudflare.com/ssl/edge-certificates/caa-records/](https://developers.cloudflare.com/ssl/edge-certificates/caa-records/)

Try adding the following CAA records to your DNS:

<table><thead><tr><th width="98">Name</th><th width="77.33333333333331">Type</th><th width="66">Flag</th><th width="105">Tag</th><th width="332">Value</th><th>TTL</th></tr></thead><tbody><tr><td>@</td><td>CAA</td><td>0</td><td>issue</td><td>"pki.goog; cansignhttpexchanges=yes"</td><td>60</td></tr><tr><td>@</td><td>CAA</td><td>0</td><td>issuewild</td><td>"pki.goog; cansignhttpexchanges=yes"</td><td>60</td></tr></tbody></table>

