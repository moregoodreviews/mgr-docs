---
description: >-
  Assign locations to your review page and enable the location picker so
  customers can choose which location they're reviewing.
icon: map-pin
---

# Locations

If your project has [locations](../projects/locations.md), you can assign them to a review page and optionally let customers choose which location they're reviewing. This helps you collect and segment reviews by store, branch, or site.

---

### Assigning Locations to a Review Page

In the **Locations** section, select which locations should use this review page. A location can only be assigned to one review page. If a location isn't assigned to any page, it uses your default review page.

When you assign locations, you'll see a table with each location and quick links to:
* **Review page** – The URL for that location (includes `?location=slug` so reviews are attributed correctly).
* **Kiosk page** – A simplified view for in-store tablets or displays.

Use these links in receipts, signage, or when requesting reviews manually for a specific location.

{% hint style="info" %}
Assigning locations to a review page is required before you can use location-specific QR codes or the location picker.
{% endhint %}

---

### Location Picker

The **Location picker** lets customers choose which location they're reviewing when they visit the page. This is useful when:

* One review page serves multiple locations (e.g., a shared link)
* Customers might have visited different stores and need to select the right one

When enabled, customers see a dropdown at the top of the form. They pick a location before selecting a rating. The review is then attributed to that location.

* **Enable / Disable** – Turn the location picker on or off.
* **Label** – The text shown above the dropdown (e.g., "Which location did you visit?").

If the link includes `?location=slug`, that location is pre-selected so the customer doesn't have to choose.

{% hint style="success" %}
Use the location picker when you have one link for many locations (e.g., on your website). Use location-specific links (`?location=slug`) when you know the location in advance (e.g., on a receipt or in-store sign).
{% endhint %}

---

### How It Works With Project Locations

Locations are created in **Settings > Locations**. Once you have locations, you can:

1. Assign them to review pages (each location uses one page)
2. Enable the location picker so customers can select a location
3. Use location-specific URLs for receipts, QR codes, and signage
4. Filter reviews, messages, and dashboard stats by location

---

### Tips

{% hint style="info" %}
If you have many locations, consider grouping them with different review pages. For example, use one page for retail stores and another for service locations.
{% endhint %}
