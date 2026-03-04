---
description: >-
  Get from signup to your first review. Covers the Get Started checklist,
  Automate button, quick path, and common blockers.
icon: list-check
---

# Getting Started

This guide gets you from signup to your first review. It's written for business owners using MGR to collect reviews for their own business. After you sign up and create a project, MGR shows a **Get Started Checklist** on your dashboard. The checklist walks you through six steps before you turn on automatic review collection. You can also request reviews manually at any time—the checklist simply helps you get everything in place first.

### Before You Start

1. **Sign up** at [moregoodreviews.com](https://moregoodreviews.com/signup) or log in if you already have an account.
2. **Create a project.** A project represents your business and can have multiple locations inside it (e.g., several storefronts). You'll be prompted to create one when you first sign up.
3. **Open your dashboard.** The Get Started Checklist appears in the bottom-left corner when you have a new project.

### Where to Find the Checklist

The Get Started Checklist appears as a collapsible panel in the bottom-left corner of your dashboard when you have a new project. Click the header to expand or collapse it. Each task has a short description and a button to jump to the relevant page. When you complete a task, it’s marked with a check. You can hide the checklist at any time; it will stop showing once your project is fully onboarded.

---

## The Checklist Steps

The checklist walks you through six steps in order:

### 1. Create a Project

A project represents your business and can have multiple locations inside it (e.g., several storefronts). Go to **Settings** to configure your project name, business info, and other basics.

### 2. Import Customers

To request reviews, MGR needs your customers’ contact information (name, email, or phone). You can import customers manually, upload a CSV, connect Stripe or HubSpot, use an app connector like Zapier, or BCC your project email when sending invoices to your customers. See [Importing Customers](importing/customers.md) for details.

### 3. View Strategy

Your **Request Strategy** controls when customers receive review requests—for example, after a charge, on a signup anniversary, or based on subscription status. MGR starts you with a default strategy; you can customize triggers, delays, reminders, and conditions in **Settings > Strategy**. See [Request Strategy](platform/request-strategy.md) for the full picture.

### 4. View Email Templates

Your request and reminder templates are what customers see in their inbox. Both include a one-click rating option and customizable text. You can add your logo and branding. Go to **Settings > Email** to edit templates and send test emails before going live.

### 5. Customize Review Page

Your review page is where customers land when they click a link. They select a rating, then see a form, links to third-party review sites (Google, Yelp, etc.), or a redirect—depending on your setup. Go to **Review Pages** to customize text, layout, form fields, links, and redirects.

### 6. Automate

The final step is turning on automatic review collection. Once you’ve completed the steps above, click **Automate** in the checklist (or in the sidebar) to enable it. MGR will start sending review requests to your customers based on your strategy.

---

## What Happens Next

After you turn on Automate, MGR sends review requests based on your [Request Strategy](platform/request-strategy.md). Requests may be delayed—for example, if your strategy sends a few days after a charge, customers won't receive a request immediately.

**Where to watch your progress:**

* **Messages** – See which requests have been sent, scheduled, opened, or clicked. Filter by status to track delivery.
* **Reviews** – New reviews appear here as customers leave feedback. Your first review is the big milestone.
* **Dashboard** – Get a quick overview of reviews, customers, and message activity.

---

## Quick Path (Minimum Setup)

If you want to get up and running as fast as possible:

1. **Import customers** – Connect Stripe or HubSpot, or upload a CSV. You need at least some customers before Automate can send anything.
2. **Add at least one link** to your review page – Go to **Review Pages** > your page > **Links**. Add a link to Google (the most important review site for most businesses). You can also connect [Google My Business](platform/integrations.md) in **Settings > Integrations** to sync and reply to Google reviews from MGR.
3. **Turn on Automate** – Click the Automate button in the sidebar and enable automatic review collection.

You can refine your strategy, templates, and review page later. This minimum setup gets requests flowing.

---

## The Automate Button in the Sidebar

The **Automate** button appears at the top of the sidebar, above Dashboard and the other navigation items. It’s the main control for automatic review collection.

### What It Does

* **When off** – The button says **Automate**. Click it to open a modal where you can enable automatic review collection. The modal shows how many customers will receive a request when you turn it on, and it links to your strategy and templates so you can review them first.
* **When on** – The button says **Automating** and turns green with a subtle animated border. Click it again to open the same modal, where you can disable automatic review collection if you need to pause it.

### How Automatic Review Collection Works

When you enable it, MGR continuously sends review requests to your customers based on your [Request Strategy](platform/request-strategy.md). Each customer is asked at most once per project (unless you manually request again). MGR can send up to three reminders if they haven’t responded. Customers can unsubscribe at any time.

The sidebar also shows how many **requests left this month** you have on your plan. This helps you stay within your plan limits.

### Tips

{% hint style="success" %}
Complete the checklist steps before turning on Automate. That way your strategy, templates, and review page are set up correctly before requests go out.
{% endhint %}

{% hint style="info" %}
You can still request reviews manually from the Customers page even when automatic collection is off. Use Automate when you’re ready to let MGR handle it for you.
{% endhint %}

{% hint style="warning" %}
When the sidebar is collapsed, the Automate control appears as a circular icon. Hover over it to see the tooltip: "Automatic Review Collection."
{% endhint %}

---

## Common Blockers

* **No customers imported** – Automate can't send requests without customers. Import at least a few before turning it on.
* **No links on your review page** – If customers give a positive rating but your review page has no links to Google (the most important), Yelp, etc., they have nowhere to leave a public review. Add at least one link in **Review Pages** > your page > **Links**.
* **Plan limits** – Check **requests left this month** in the sidebar. If you've hit your limit, you may need to upgrade your plan.

---

## Need Help?

If you get stuck, click the help bubble on the site to reach us. We're here to help you get the most out of MGR.
