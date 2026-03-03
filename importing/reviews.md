---
description: >-
  Bring existing reviews into MGR from Google, Facebook, Trustpilot, Yelp,
  LinkedIn, CSV upload, or manual entry.
icon: file-import
---

# Importing Reviews

If you have reviews on Google, Facebook, Yelp, or other sites, you can bring them into MGR so they appear in your dashboard and on your [Showcase](../platform/showcase.md). This page explains where to find the import options and how each method works.

### Where to Import

Go to **Reviews** in the sidebar and click **Add**. A modal opens with three tabs: **Quick Import**, **Manual Entry**, and **Upload CSV**.

---

### Quick Import (from a Website URL)

Import reviews directly from a public review page. Paste the URL and MGR will fetch the reviews for you.

**Supported sites:** Google, Facebook, Trustpilot, Yelp, LinkedIn

**Steps:**

1. Go to **Reviews** and click **Add**.
2. Open the **Quick Import** tab.
3. Under **Website**, choose the review site (Google, Facebook, Trustpilot, Yelp, or LinkedIn).
4. Paste the URL of your business's review page. The placeholder shows the format—for example, your Google Maps place URL or your Facebook reviews page.
5. If you use locations, optionally assign the imported reviews to a location.
6. For Google, Facebook, Trustpilot, and Yelp, you can check **Positive only** to import only 4- and 5-star reviews.
7. Click **Import Recent Reviews**.

The import runs in the background. You'll see a confirmation when it's scheduled. Reviews appear in your list shortly after. You may receive an email when the import completes.

{% hint style="info" %}
For Google reviews, you can also connect **Google My Business** under **Settings > Integrations** to sync reviews automatically on an ongoing basis.
{% endhint %}

{% hint style="warning" %}
The URL must point to a public review page. If the page structure changes or the site blocks the import, the import may fail. You'll receive an email if that happens.
{% endhint %}

---

### Manual Entry

Add one review at a time. Enter the customer's name, contact info, rating, review text, date, and optionally the source, location, and tags.

**Steps:**

1. Go to **Reviews** and click **Add**.
2. Open the **Manual Entry** tab.
3. Fill in the customer section (first name, last name, email, phone, company).
4. Fill in the review section (rating, review text, date, source, location, tags).
5. Click **Save**.

The review appears in your list immediately.

{% hint style="info" %}
Manual entry is ideal when you have a few reviews or want to add one quickly. For larger batches, use Quick Import or CSV upload.
{% endhint %}

---

### CSV Upload

Upload a CSV file to import up to 1,000 reviews at once. The import runs in the background; you'll see a confirmation when it's scheduled. Reviews appear in your list shortly after. You may receive an email when the import completes.

**Steps:**

1. Go to **Reviews** and click **Add**.
2. Open the **Upload CSV** tab.
3. Click **Download Template** to get a sample file with the correct headers.
4. Fill in your data and save as CSV (UTF-8).
5. Click **Upload CSV** and select your file.

**CSV Headers**

| Header | Required | Description |
|--------|----------|-------------|
| first_name | Yes | The reviewer's first name. |
| last_name | No | The reviewer's last name. |
| email | No | The reviewer's email address. |
| phone | No | The reviewer's phone number. |
| company | No | The reviewer's company name. |
| score | Yes | The rating (1–5). |
| review | No | The review text. |
| source | No | The slug or UUID of a source. Must match a source in **Settings > Sources**. |
| location | No | The slug or UUID of a location. Must match a location in **Settings > Locations**. |
| tags | No | Comma-separated list of tag slugs. Tags must exist in your project and be for reviews. |
| created_at | No | The date of the review. Use YYYY-MM-DD format. |

**What happens during import:** Each row creates or finds a customer (by email or phone) and attaches a review to them. If the customer already exists, the review is added to their profile. If not, a new customer is created.

{% hint style="warning" %}
Each row must have either an email or a phone number so MGR can associate the review with a customer. Without a way to identify the reviewer, the import may skip or fail for that row.
{% endhint %}

{% hint style="info" %}
Download an example CSV template from [moregoodreviews.com/csv/reviews.csv](https://moregoodreviews.com/csv/reviews.csv).
{% endhint %}

---

### After Import

* **Quick Import** – The import runs in the background. You may receive an email when it completes. Reviews appear on the Reviews page as they are processed.
* **CSV Upload** – Same as Quick Import. The import is scheduled and runs in the background.
* **Manual Entry** – The review appears immediately.

Once reviews are in your project, they appear in your [Showcase](../platform/showcase.md), widgets, and analytics. You can reply to them, assign tags, or filter by location.

---

### Tips

{% hint style="success" %}
Use the **Positive only** option when importing from Google, Facebook, Trustpilot, and Yelp if you want to focus on 4- and 5-star reviews for your showcase or marketing.
{% endhint %}

{% hint style="info" %}
If you have multiple locations, assign a location when importing so you can filter and report by location later.
{% endhint %}

{% hint style="info" %}
Tags in the CSV must use tag slugs (the URL-friendly name) and must already exist in your project under Settings > Tags. Use comma-separated values for multiple tags. Tags must be for reviews, not customers.
{% endhint %}
