---
icon: code
---

# Widgets

You can display your reviews on your website using our custom widget builder. We offer a variety of widget types to choose from. To get started, go to the [Widgets](https://moregoodreviews.com/widgets) page in the sidebar and click Create Widget.

Available widget types:

<table data-view="cards"><thead><tr><th></th><th></th></tr></thead><tbody><tr><td><strong>Badge</strong></td><td>A compact style aggregate of your reviews.</td></tr><tr><td><strong>Carousel</strong></td><td>A rotating horizontal slider featuring hand-selected reviews.</td></tr><tr><td><strong>Dynamic Carousel</strong></td><td>A rotating horizontal slider that automatically updates to display the latest reviews.</td></tr><tr><td><strong>Corner</strong></td><td>A corner popup on your website displaying a rotating list of reviews.</td></tr><tr><td><strong>Dynamic Corner</strong></td><td>A corner popup on your website that automatically updates to display the latest reviews.</td></tr><tr><td><strong>Faces</strong></td><td>The faces of the customers that left reviews.</td></tr><tr><td><strong>Headline</strong></td><td>An aggregate of all your reviews.</td></tr><tr><td><strong>Highlights</strong></td><td>A continuously scrolling display featuring hand-selected review highlights.</td></tr><tr><td><strong>Marquee</strong></td><td>A continuously scrolling display featuring hand-selected reviews.</td></tr><tr><td><strong>Spotlight</strong></td><td>A singular featured review with emphasis.</td></tr><tr><td><strong>Wall</strong></td><td>A paginated masonry grid layout that automatically updates to display the latest reviews.</td></tr></tbody></table>

### Customizing Widgets

The left sidebar is composed of several expandable panels to help you filter and customize your widgets to fit your own unique branding and style guidelines. These options can vary depending on the widget you are building. The following is a list of all possible options available to you:

**Reviews**

* Review IDs - Some widgets may require you to select one or more reviews to display.
* Review ID - Some widgets may require you to select just one review to display.

**Layout**

* Alignment - Left or centered layout.
* Source - Show or hide the source.
* Source Position - The placement of the source.
* Date - Show or hide the date of the review.
* Quotes - Surround the review in quotation marks.
* Shorten Review - Truncate the review.
* Padding - Spacing around the content.
* Review Count - Show or hide the number of reviews.

**Color**

* Star Color - The color of the stars.
* Text Color - The color of the text.
* Background Color - The color of the background.
* Border Color - The color of the border.

**Font**

* Font Family - The system of Google font to use.
* Font Size - The font size in pixels.

**Rating**

* Star Display - Show, hide, or only show full stars.
* Star Size - The size of the stars in pixels.

**Customer**

* Name - First name, First name with last initial, initials, or hide.
* Avatar - Show, hide, or only show if the photo is available.
* Customer Position - Top or bottom of widget.
* Company - Show or hide the company.

**Border**

* Border Radius - The size of the border radius in pixels.
* Border Width - The width of the border in pixels.
* Drop Shadow - Show or hide a drop shadow.

**Carousel**

* Autoplay - Enable or disable.
* Autoplay Delay - The timing between slide transitions.
* Pagination - Show arrows, dots, or hide pagination.
* Max Slides - The maximum number of slides to display on a page.

**Animation**

* Delay - Seconds to wait before showing each review.

**Marquee**

* Visible Slides - How many reviews are visible at once.
* Duration - The speed of the scrolling track.

**Filters**

* Reviews Per Page - For paginated results, the number of reviews per page.
* Maximum Reviews - The maximum number of reviews to display. 0 means no maximum.
* Lowest Rating - Show reviews with X score or higher.
* Review Length - Show reviews with X characters or more.
* Locations - Show reviews for specific locations.
* Sources - Show reviews from specific sources.
* Tags - Show reviews with specific tags.
* Include Hidden – Choose whether to display hidden reviews. Defaults to No.

**Schema**

* Schema - Include or exclude JSON-LD [markup](https://schema.org/AggregateRating) to potentially show a star rating in Google search.
* Business Type - The business type for the markup.
* Business Name - The business name for the markup.

### Embedding Widgets

Embedding a widget on your website is as simple as copying and pasting a single line of code into your HTML or CMS. The code block is visible right in the footer of the builder.

If you place the embed code within the `<body>` tag, the widget will appear exactly where it’s inserted.

If you place the code in the `<head>` tag, the widget will render at the top of the page, just after the opening `<body>` tag. To control where it appears in this case, add a `data-target` attribute to the embed code and set it to the ID of the element where you want the widget to display.

For example:

```html
<head>
<script id="[WIDGET-UUID]" src="https://tag.moregoodreviews.com/js/app.js" data-target="widget-container"></script>
</head>
```

If a div with id widget-container exists on your page, the widget will render there.

```html
<body>
<div id="widget-container"><!-- widget will render here --></div>
</body>
```

### Restricting Widgets

#### Allowed Domains

By default, widgets can be embedded on any website. You can set allowed domains for your widgets to ensure only approved websites can display your reviews. When editing a widget, click on the Actions menu, and then Settings. Enter one or more allowed domains in the field.

#### Language

By default, all widget text (excluding reviews, customer names, and sources) matches the visitor’s browser language. You can override this by setting a specific language instead of using auto-detect. When editing a widget, click on the Actions menu, and then Settings. Select a language from the dropdown menu.

### Publishing Widgets

When editing widgets, all changes are applied live in real time. However, you can easily publish or unpublish a widget from the widget builder. Unpublishing a widget will hide it from your website while you continue working on it. If your account has a widget limit, any new widgets created beyond that limit will remain unpublished until you upgrade your plan.
