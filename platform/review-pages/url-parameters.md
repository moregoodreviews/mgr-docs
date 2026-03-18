---
description: >-
  Pre-fill location, rating, name, email, and more by adding parameters to
  your review page or kiosk URL.
icon: globe
---

# URL Parameters

You can add parameters to your review page URL (or kiosk link) to pre-fill or pre-select information when customers visit. This saves customers time and ensures reviews are attributed correctly. Append parameters using `?` for the first parameter and `&` for additional ones.

---

### Location

Add `location=slug` to send customers to a specific location. The location picker (if enabled) will show that location as already selected, and the review will be attributed to it. Use the location's slug from your [Locations](locations.md) settings.

Example: `yoursite.com/review?location=downtown`

---

### Form

If you have multiple review pages, add `form=123` (using your review page's ID) to show a specific page instead of the default. Useful when different campaigns or channels use different pages.

---

### Rating

Add `score=5` (or 1–5) to pre-select a rating. Customers see that rating already chosen when they arrive. Often used in email or SMS links where you want to emphasize a positive rating.

---

### Tags

Add `tags=slug1,slug2` to tag reviews that come from that link. Helps you segment feedback in reports (e.g., "in-store" vs "online").

---

### Name, Email, Phone

Add `first_name`, `last_name`, `email`, or `phone` to pre-fill those form fields. Useful when you have customer info from another system (e.g., a booking or checkout) and want to pass it into the review link.

Example: `yoursite.com/review?first_name=Jane&email=jane@example.com`

---

### Combining Parameters

You can combine any of these parameters in a single URL:

`yoursite.com/review?location=downtown&score=5&first_name=Jane&email=jane@example.com`

{% hint style="info" %}
Links sent via email or SMS include a token that automatically pre-fills the customer's name and email. No need to add those as URL parameters when using tracked links.
{% endhint %}

{% hint style="success" %}
Use location-specific links on receipts, table tents, or in-store signage so reviews are attributed to the right store. Combine with `score=5` to encourage positive ratings and build your reputation.
{% endhint %}
