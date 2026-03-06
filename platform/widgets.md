---
description: >-
  Display your reviews, ratings, and feedback on your website with embeddable
  widgets. Badge, Carousel, Wall, Corner, and more.
icon: code
---

# Widgets

Widgets let you display your reviews, ratings, and feedback on your website. Create a widget in the builder, customize its appearance to match your brand, then copy the embed code and paste it into your site. Visitors see your reputation and testimonials right where they browse—helping build trust and drive conversions.

### Where to Find Widgets

Go to **Widgets** in the sidebar and click **Create Widget** or **Add**. Choose a widget type, give it a name, and you're taken to the builder. From there you can customize the design, preview it on desktop or mobile, and copy the embed code.

---

## Widget Types

Each widget type has a different layout and purpose. Some show a summary of your ratings; others display individual reviews or a rotating selection. Choose the one that fits your page and goals.

### Badge

A compact summary of your reviews. Shows your average star rating, total review count, and optionally the source logos (Google, Yelp, etc.). Ideal for sidebars, footers, or anywhere you want a small trust signal without taking much space.

### Headline

A bold headline-style display of your average rating and total review count. No individual reviews—just the headline numbers. Great for landing pages or hero sections where you want to lead with your reputation.

### Faces

A row of customer photos (avatars) from reviewers who have profile pictures. Shows the faces behind your reviews with your average rating and count below. Perfect for adding a human touch and social proof.

### Spotlight

A single featured review in a prominent layout. Ideal when you want to highlight one standout testimonial or piece of feedback. You choose which review to display.

### Carousel

A horizontal slider of hand-selected reviews. You pick the reviews to show, and they rotate with arrows or dots for navigation. Good for showcasing your best feedback in a controlled way.

### Dynamic Carousel

A horizontal slider that automatically updates to show your latest reviews. No need to manually pick reviews—it pulls new ones as they come in. Use this when you want fresh content without maintenance.

### Marquee

A continuously scrolling display of hand-selected reviews. Reviews scroll horizontally across the page in a ticker-style layout. Good for high-energy or busy pages where you want constant motion.

### Highlights

A continuously scrolling display of short review excerpts. You pick the reviews to show, and only the text you've highlighted in each review appears—for example, a key phrase like "best service ever" or "highly recommend." Useful for quick, punchy snippets of feedback.

{% hint style="warning" %}
**Manual highlighting required.** The Highlights widget only shows the text you've manually highlighted in each review. Go to **Reviews**, open a review, select the phrase or sentence you want to feature, and apply the highlight (using the highlight tool in the review editor). Save the review. Then add that review to your Highlights widget. If you don't highlight any text in a review, nothing from that review will appear in the widget.
{% endhint %}

### Wall

A paginated masonry grid of reviews that automatically updates with your latest feedback. Visitors can browse through pages of reviews. Best for dedicated review pages or when you want to show many testimonials at once.

### Corner

A corner popup that appears on your site after a short delay. Shows a rotating list of hand-selected reviews. Use it to draw attention to feedback without blocking the main content.

### Dynamic Corner

A corner popup that automatically updates to display your latest reviews. Same as Corner, but it pulls new reviews automatically.

{% hint style="info" %}
**Hand-selected vs. dynamic:** Carousel, Marquee, Highlights, and Corner widgets let you pick which reviews to show. Dynamic Carousel, Dynamic Corner, and Wall widgets automatically show your latest reviews based on your filter settings.
{% endhint %}

---

## Creating and Editing Widgets

1. Go to **Widgets** and click **Create Widget** or **Add**.
2. Enter a name and choose a widget type.
3. Click **Create**.
4. You're taken to the builder. The left sidebar has expandable panels for customization; the right side shows a live preview.

Changes appear in real time as you adjust settings. Click **Save** when you're done. Use the desktop and mobile icons in the toolbar to preview how the widget looks on different screen sizes.

{% hint style="success" %}
Use the canvas color picker in the toolbar to preview your widget against a background that matches your site. This helps you see how colors and borders will look in context.
{% endhint %}

---

## Customization Options

The builder sidebar has several expandable panels. The options you see depend on the widget type. Here's what each group controls:

### Reviews

* **Review** — For Spotlight: pick the single review to display.
* **Reviews** — For Carousel, Marquee, Highlights, and Corner: pick the reviews to display. For Highlights, only reviews where you've manually highlighted text will show excerpts; unhighlighted reviews won't appear.
* **Reviews for Faces** — For Faces: pick which reviews to show customer photos from.

### Layout

* **Alignment** — Left or centered.
* **Review Count** — Show or hide the total number of reviews.
* **Source** — Show or hide where the review came from (e.g., Google, Yelp).
* **Source Position** — Place the source in the footer or next to the avatar.
* **Date** — Show or hide when the review was written.
* **Shorten Review** — Truncate long reviews.
* **Padding** — Spacing around the content.
* **Width** — For Corner: set the popup width.
* **Show on Mobile** — For Corner: show or hide the popup on phones.

### Colors

* **Star Color** — Color of the stars.
* **Text Color** — Color of the text.
* **Background Color** — Color of the background.
* **Border Color** — Color of the border.

### Font

* **Font Family** — System font or Google font.
* **Font Size** — Size in pixels.
* **Font Emphasis** — None, bold, italic, or underline (for Headline).

### Rating

* **Star Display** — Show all stars, show full stars only, or hide stars.
* **Star Size** — Size in pixels.

### Customer

* **Name** — Full name, first name with last initial, initials, or hidden.
* **Avatar** — Show avatar, show only when photo is available, or hide.
* **Customer Position** — Top or bottom of the review card.
* **Company** — Show or hide the company name.

### Border

* **Border Radius** — Corner roundness in pixels.
* **Border Width** — Border thickness in pixels.
* **Drop Shadow** — Show or hide a drop shadow.

### Carousel

* **Autoplay** — Enable or disable automatic rotation.
* **Autoplay Delay** — Seconds between slide transitions.
* **Pagination** — Arrows, dots, or hidden.
* **Max Slides** — How many reviews to show at once on larger screens.

### Animation

* **Delay** — For Corner: seconds to wait before the popup appears.

### Marquee

* **Visible Slides** — How many reviews are visible at once.
* **Duration** — Speed of the scrolling animation.

### Filters

For dynamic widgets (Wall, Dynamic Carousel, Dynamic Corner) and aggregate widgets (Badge, Headline, Faces):

* **Reviews Per Page** — For Wall: how many reviews per page.
* **Maximum Number of Reviews** — Cap total reviews shown. 0 means no limit.
* **Lowest Rating** — Only show reviews with this score or higher.
* **Review Length** — Only show reviews with at least this many characters.
* **Locations** — Show reviews from specific locations.
* **Sources** — Show reviews from specific sources (e.g., Google only).
* **Tags** — Show reviews with specific tags.
* **Include Hidden Reviews** — Show or hide reviews you've marked as hidden.

### Schema

For Badge and Wall:

* **Schema** — Include or exclude structured data so search engines can show a star rating in search results.
* **Business Type** — LocalBusiness, SoftwareApplication, Product, Service, or Course.
* **Business Name** — Name used in the structured data.

{% hint style="info" %}
Schema markup helps search engines understand your ratings. When enabled, it can lead to star ratings appearing in Google search results. For more on this, see [schema.org AggregateRating](https://schema.org/AggregateRating).
{% endhint %}

---

## Embedding Widgets

Copy the embed code from the builder footer and paste it into your site. The code is a single line—paste it into your HTML or CMS. The widget will appear where you insert it.

**Placement in body:** If you put the code inside the `<body>` tag, the widget appears exactly where it's inserted.

**Placement in head:** If you put the code in the `<head>` tag, the widget renders at the top of the page, just after the opening `<body>` tag. To control where it appears, add a `data-target` attribute and set it to the ID of the element where you want the widget to display.

For example, if you want the widget inside a div with id `widget-container`, add `data-target="widget-container"` to the script tag. The widget will render inside that div.

{% hint style="info" %}
Use the **Embed** option in the Actions menu to open the embed modal. You can choose body or head placement and, for head placement, specify the container ID. The modal shows the correct code for your choice.
{% endhint %}

---

## Widget Settings

Click **Actions** in the builder toolbar and choose **Settings** to open the widget settings:

* **Name** — Change the widget name.
* **Language** — By default, widget text (labels, buttons, etc.) matches the visitor's browser language. You can override this and set a specific language.
* **Allowed Domains** — By default, widgets can be embedded on any website. Add one or more allowed domains in Settings to restrict where the widget can appear. Only approved domains will be able to display your reviews.

{% hint style="warning" %}
If you set allowed domains, the widget will not load on sites that aren't in the list. This helps prevent unauthorized use of your reviews.
{% endhint %}

---

## Publishing and Unpublishing

Widgets can be published or unpublished. Use the **Published** toggle in the builder or on the Widgets list. When published, the widget appears on your site. When unpublished, it's hidden—visitors won't see it, but you can still edit it.

If your plan has a widget limit, new widgets created beyond that limit stay unpublished until you upgrade. You can still build and customize them; they just won't display until you're within your limit and publish them.

---

## Actions

From the builder or the Widgets list:

* **Copy Embed Code** — Open the embed modal to copy the code for your site.
* **Restore to Defaults** — Reset design settings (colors, fonts, layout) to their defaults. Filter settings (reviews, locations, tags) are kept.
* **Settings** — Edit name, language, and allowed domains.
* **Duplicate** — Create a copy of the widget with the same settings.

---

## Tips

{% hint style="success" %}
Combine widgets for different pages. Use a Badge in your footer, a Wall on a dedicated testimonials page, and a Corner in your checkout flow for maximum impact.
{% endhint %}

{% hint style="info" %}
Enable Schema for Badge and Wall widgets if you want star ratings to appear in Google search results. Set the Business Type and Business Name to match your business.
{% endhint %}

{% hint style="info" %}
Use filters to narrow which reviews appear. For example, show only 4- and 5-star reviews, or only reviews from Google or a specific location.
{% endhint %}

{% hint style="info" %}
For the **Highlights** widget, remember to highlight the exact text you want in each review before adding it to the widget. Open each review from **Reviews**, select the phrase or sentence, apply the highlight, and save. The widget displays only that highlighted text.
{% endhint %}

{% hint style="info" %}
The Widgets page is separate from the [Showcase](showcase.md). Widgets are embedded on your own site; the Showcase is a dedicated page at its own URL. Both can help build trust and reputation.
{% endhint %}
