---
description: >-
  Configure the template, instructions, rating options, and email notifications
  for your review page.
icon: settings
---

# Settings

The **Settings** section controls the main content and behavior of your review page. It includes four parts: **Template**, **Instructions**, **Options**, and **Notifications**.

---

### Template

The template defines the core text and structure customers see:

* **Name** – The internal name for this review page (e.g., "Main Feedback Form"). Used in the app, not shown to customers.
* **Title** – The headline at the top of the page. Often a question, like "How was your experience?"
* **Introduction** – A short paragraph below the title inviting customers to leave feedback.
* **Footer** – Optional text at the bottom, such as a disclaimer or legal information.
* **Button Label** – The text on the submit button (e.g., "Submit" or "Send Feedback").

---

### Instructions

Instructions appear directly above the form after a customer selects a rating. You can set different instructions for each rating level. For example:

* For a 5-star rating: "Thanks! Please share your experience so others can learn from it."
* For a 1-star rating: "We're sorry to hear that. Tell us what went wrong so we can improve."

Use the tabs to switch between ratings and edit the instructions for each. This lets you tailor the message based on whether the customer had a positive or negative experience.

---

### Options

These options control how ratings and reviews work:

* **Rating selection** – When to save the rating:
  * **Save rating before customer review** – Only when the customer arrives via email, SMS, or a direct customer link. Anonymous visitors don't have their rating saved until they submit the form.
  * **Save rating before every review** – Save the rating for anyone who visits the page, including anonymous visitors.
  * **Never save rating before review** – Only save the rating when the customer submits the form or leaves a written review.

* **Native reviews** – Whether to accept written reviews (testimonials) on your page. If disabled, customers who give a positive rating will only see links to third-party sites (you must add at least one [Link](links.md) or [Redirect](redirects.md)). Negative ratings still show the feedback form.

* **Editable ratings** – Whether customers can change their rating immediately after selecting it. If disabled, they must refresh the page to pick a different rating.

{% hint style="info" %}
If you disable native reviews for positive ratings, make sure you have links or redirects configured. Otherwise, customers who select a positive rating will have nothing to click.
{% endhint %}

---

### Notifications

Enter one or more email addresses (separated by commas) to receive a notification whenever someone submits a review on this page. Useful for staying on top of new feedback, especially negative reviews that need a quick response.

---

### Tips

{% hint style="success" %}
Use the instructions to set expectations. For negative ratings, a short "We're sorry—please tell us more" can encourage detailed feedback you can act on.
{% endhint %}

{% hint style="info" %}
Keep the introduction brief. Customers are more likely to complete the form when the page is easy to scan.
{% endhint %}
