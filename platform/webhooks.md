---
description: Add webhooks to your project to receive events about reviews and messages.
icon: webhook
---

# Webhooks

You can add one or more webhook URLs in order to receive events from the platform. Simply add your webhook URLs in the API settings page, [here](https://moregoodreviews.com/settings/api#webhooks).

1. review-created - Fired when a review has been created.
2. review-updated - Fired when a review has been updated.
3. review-deleted - Fired when a review has been deleted.
4. message-created - Fired when a message has been created.
5. message-updated - Fired when a message has been updated.
6. message-deleted - Fired when a message has been deleted.

### Review Events

It is important to note that a review is saved immediately upon clicking a link that contains a score in the parameter. For example, when an email is sent to a customer asking for their review, they may select a rating that takes them to your review page. Once the page loads, that rating is captured and a new review has been made. They may then add to that review by saving their feedback or positive review in the native review box. In this scenario, you will get a ping when the review is created, and then a 2nd ping when the review is updated.
