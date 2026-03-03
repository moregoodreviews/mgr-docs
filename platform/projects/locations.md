---
description: >-
  Create and manage locations for multi-location businesses. Assign review
  pages, filter data by location, and attribute reviews and feedback to
  specific stores or branches.
icon: map-marker
---

# Locations

Locations let you manage multiple stores, branches, or sites within a single project. Each location can have its own review page, address, and link. Reviews, messages, and dashboard stats can be filtered by location so you can see performance for each one. Locations are useful for businesses with more than one physical location—restaurants, retail chains, service areas, and more.

### Where to Find Locations

Go to **Settings** in the sidebar, then click **Locations**. You'll see a list of your locations. If you don't have any yet, you'll see a notice with a button to create your first one.

{% hint style="info" %}
Locations are an optional add-on on some plans. If the section is locked, you may need to upgrade to use them.
{% endhint %}

---

### Creating a Location

1. Click **Add** (or **Create location** if you have none).
2. Enter a **Name** for the location (e.g., "Downtown Store" or "Main Office"). This is required.
3. Click **Create**.

Your new location appears in the list. Click it to edit and add more details.

---

### Editing a Location

Click a location or its **Edit** button to open the edit modal. You can configure:

#### Settings

* **Name** – The internal name for the location. Used in filters and reports.
* **Display name** – Optional. A different name shown to customers (e.g., on the review form). If left blank, the name is used.
* **Slug** – A short identifier used in URLs. For example, a slug of `downtown` makes the review link `yoursite.com/review?location=downtown`. Slugs are usually auto-generated from the name but you can change them. Each slug must be unique within the project.
* **Store code** – Optional. A code, SKU, or identifier for the location (e.g., "STORE-001"). Useful for reporting or integrations.
* **Review page** – Which review page this location uses. Customers directed to this location will see that page. A location can only be assigned to one review page.

#### Address

Expand the **Address** section to add the location's physical address:

* Address line 1 and 2
* City
* State or region
* Postal code

The address is used in email templates (e.g., the `{{location_address}}` placeholder) and can help with integrations.

#### Integrations

If the location is connected to an integration (such as Google My Business), you'll see it listed here. Integrations are set up elsewhere; this section is informational.

When you're done, click **Save**. To remove a location, click **Delete** in the footer. You'll be asked to confirm.

{% hint style="warning" %}
Deleting a location is permanent. Reviews and messages already tied to that location will keep the association, but you won't be able to assign new data to it.
{% endhint %}

---

### How Locations Are Used

Once you have locations, they appear throughout the project:

#### Review Pages

In each review page's settings, you can **assign locations** to that page. A location can only use one review page. If a location isn't assigned to any page, it uses the default review page.

You can also enable a **Location picker** on a review page. When enabled, customers see a dropdown to choose which location they're reviewing. This is useful when one review page serves multiple locations (e.g., a shared link). If the link includes `?location=slug`, that location is pre-selected.

#### Review Links

Add `?location=slug` to your review page URL to send customers directly to a specific location. For example:

`yoursite.com/review?location=downtown`

Any review submitted from that link is attributed to the Downtown location.

#### Manual Review Requests

When you request a review from a customer's profile, you can choose a **Location** in the options. The review link in the message will point to that location.

#### Dashboard and Reports

On the dashboard, you can filter stats by location to see reviews, ratings, and message counts for each one. The same filter appears on the Messages page, Reviews page, and elsewhere—so you can focus on a single location or compare them.

#### Showcase

You can limit your public Showcase to specific locations. That way, visitors see only reviews for the locations you choose.

#### QR Codes

When generating a QR code for a review page, you can select a location. The QR code will link to that location's review page, so you can place different codes at different stores.

---

### Tips

{% hint style="info" %}
Use clear, consistent names for locations. If you have many, consider a naming pattern (e.g., "City - Street" or "Region #1") to keep things organized.
{% endhint %}

{% hint style="info" %}
The slug appears in URLs. Keep it short and readable—customers may see it. Use lowercase letters and hyphens (e.g., `main-street`).
{% endhint %}

{% hint style="success" %}
Assign each location to the review page that fits it best. You might use different pages for different regions, services, or languages.
{% endhint %}

{% hint style="info" %}
If you have one review page for many locations, enable the Location picker so customers can choose where they're leaving feedback. Use location-specific links (`?location=slug`) when you know the location in advance—for example, in receipts or in-store signage.
{% endhint %}
