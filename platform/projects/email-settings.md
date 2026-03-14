---
description: >-
  Configure email templates and settings for sending review requests and
  reminders to customers. Customize subject lines, message content, sender
  info, and appearance.
icon: envelope
---

# Email Settings

Email settings control how your project sends review requests and reminders to customers. You can customize the message content, who the emails come from, and how they look. These settings apply to all emails sent from your project—including requests, reminders, and thank-you messages.

### Where to Find Email Settings

Go to **Settings** in the sidebar, then click **Email**. You'll see four sections: **Templates**, **Review Link**, **Appearance**, and **Settings**. Each section has its own **Save** button, so remember to click it after making changes.

---

### Templates

Templates are the actual messages your customers receive. Each template has a purpose:

* **Request** – The first email asking a customer to leave a review.
* **Reminder** – Follow-up emails sent when a customer hasn't responded yet. You can have up to three reminders, depending on your [Request Strategy](../request-strategy.md).
* **Thanks (positive)** – Sent when a customer leaves a positive rating.
* **Thanks (negative)** – Sent when a customer leaves a negative rating.

#### Editing a Template

1. Use the dropdown at the top to select which template you want to edit.
2. Edit the **Subject** line (for email templates).
3. Edit the **Body** of the message. You can use placeholders that get replaced with real data—for example, the customer's first name, your business name, or the link to leave a review.
4. Click **Save** to apply your changes.

{% hint style="info" %}
Placeholders like `{{first_name}}` and `{{project_name}}` are replaced automatically when the email is sent. Use them to personalize your messages and improve response rates.
{% endhint %}

#### Previewing and Testing

Click **Preview** to see how the email will look on desktop or mobile. You can switch between desktop and mobile views in the preview window.

To send a test email, expand **Send test** in the preview window, enter one or more email addresses (separated by commas), and click **Send**. Test emails can only be sent to project members—this helps prevent accidental sends to real customers.

{% hint style="success" %}
Send yourself a test before turning on automatic review collection. That way you can confirm the message looks right and the link works.
{% endhint %}

---

### Review Link

The **Review Link** section controls how customers respond when they receive a review request or reminder email. You choose whether they see a row of ratings to tap or a single button, and where that link takes them. These settings apply to all request and reminder templates at once—so you can keep your emails consistent without editing each template separately.

#### Link style

Choose how the main link appears in your review request and reminder emails:

* **Rating selector** – Customers see a row of stars (or other rating symbols) to tap or click. Each option links directly to your review page with that rating pre-selected. This works well when you want customers to choose a rating before they land on the form.
* **Button** – Customers see a single button with custom text. Use this when you prefer a cleaner look or want to emphasize one clear action.

{% hint style="info" %}
The rating selector shows your configured ratings (stars, faces, or custom symbols) from your [Review Pages](../review-pages/README.md) settings. The button gives you more control over the label and where it links.
{% endhint %}

#### Button Label (Button Only)

When you choose **Button**, you can customize the text that appears on it. For example: "Leave a Review", "Share Your Feedback", or "Rate Your Experience". Keep it short and action-oriented so customers know what to expect when they click.

#### Link for Button (Button Only)

When you use a button, you choose where it sends customers:

* **Review page** – The button links to your project's review page, where customers can select a rating and leave a review or feedback. This is the default and works for most businesses collecting reviews and ratings.
* **Custom URL** – The button links to a web address you specify. Use this when you want to send customers to a specific landing page, survey, or third-party review site instead of your built-in review form.

If you choose **Custom URL**, a field appears where you enter the full web address (for example, `https://your-website.com/feedback`). Make sure the link starts with `https://` and points to a page you control or trust.

{% hint style="info" %}
When using a custom URL, the link is the same for every customer—you cannot personalize it per customer. Clicks are still tracked so you can see who opened and clicked in your [Messages](messages.md) view.
{% endhint %}

{% hint style="success" %}
A clear review link improves click-through rates. Test both the rating selector and button to see which performs better for your audience and reputation goals.
{% endhint %}

---

### Settings

The **Settings** section controls who your emails come from and what appears at the bottom of each message.

* **Sender name** – The name customers see in their inbox (e.g., "Sarah from Acme Coffee"). Use a real person's name to build trust.
* **Sender email address** – The email address that appears as the sender. You can choose to send from your root domain (e.g., `reviews@yourdomain.com`) or a subdomain (e.g., `reviews@reviews.yourdomain.com`). To customize this, you must first add a [sending domain](../adding-your-domain.md).
* **Reply-to** – Where replies from customers go. Enter one or more email addresses, separated by commas (e.g., `support@yourdomain.com`).
* **Footer** – Optional text or links that appear at the bottom of every email. You can use placeholders like `{{project_name}}` and `{{current_year}}`.
* **Unsubscribe text** – The text shown for customers who want to stop receiving messages. This is required for compliance.
* **List-Unsubscribe headers** – Choose whether to include standard unsubscribe headers that help email clients show an unsubscribe option. Including them can improve deliverability.

{% hint style="warning" %}
If you haven't added a sending domain, the sender email address will use the default domain and you won't be able to change it. Add your domain in **Settings > Domain** first.
{% endhint %}

---

### Appearance

The **Appearance** section controls the visual style of your emails:

* **Text alignment** – Left or center alignment for the email content.
* **Font family** – The font used in the email body. Choose from system fonts or Google fonts.

These settings apply to all review request and reminder emails. Your logo and primary color from [Appearance](appearance.md) branding also appear in these emails.

{% hint style="info" %}
Emails that look professional and on-brand are more likely to be opened and acted on. Match your email appearance to your website and other marketing materials.
{% endhint %}

---

### How It All Works Together

1. **Templates** define what you say—the subject and body for each type of message.
2. **Review Link** defines how customers respond—rating selector or button, and where the link goes.
3. **Settings** define who the email comes from and what appears in the footer.
4. **Appearance** defines how the email looks—alignment and fonts.

When you update any of these, the changes apply to new emails only. Messages already sent or scheduled keep their original content and look.

---

### Tips

{% hint style="info" %}
Keep your subject lines short and personal. Including the customer's name or a clear benefit (e.g., "Quick favor, {{first_name}}") can improve open rates and reviews.
{% endhint %}

{% hint style="info" %}
Use the same sender name and branding across all your customer communications. Consistency builds trust and helps your reputation.
{% endhint %}

{% hint style="success" %}
Review your templates before enabling automatic review collection. The dashboard will prompt you to preview your email templates when you're ready to automate.
{% endhint %}
