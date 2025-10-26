---
description: >-
  You can use our secure REST API to import your customer data, send review
  requests, export your reviews, and more!
icon: rectangle-terminal
---

# API Reference

### Authentication

Your project has a secret API key that you can use to authenticate your requests. You can find your project’s API key, [here](https://moregoodreviews.com/settings/api).

Add your API key to the Authorization header of each request. For example:

```json
"Authorization": "Bearer <API_KEY>"
```

### Endpoints

#### Create or update a customer

<mark style="color:green;">`POST`</mark> `https://api.moregoodreviews.com/beacon/customers`

Creates a new customer or updates an existing one.

**Body**

<table data-full-width="false"><thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td>first_name*</td><td>string</td><td>The customer's first name.</td></tr><tr><td>last_name</td><td>string</td><td>The customer's last name.</td></tr><tr><td>email</td><td>string</td><td>The customer's email address.</td></tr><tr><td>phone</td><td>string</td><td>The customer's phone number.</td></tr><tr><td>company</td><td>string</td><td>The customer's company name.</td></tr><tr><td>has_subscription</td><td>boolean</td><td>Whether or not the customer is subscribed to your service.</td></tr><tr><td>location_slug</td><td>string</td><td>The slug of a <a href="https://moregoodreviews.com/settings/locations">location</a>.</td></tr><tr><td>signed_up_at</td><td>date</td><td>The date the customer signed up to your service.</td></tr></tbody></table>

#### Create a review request

<mark style="color:green;">`POST`</mark> `https://api.moregoodreviews.com/beacon/asks`

Schedules a review request for the customer.

**Body**

| Name             | Type                            | Description                                                          |
| ---------------- | ------------------------------- | -------------------------------------------------------------------- |
| email            | string, required without phone. | The customer's email address                                         |
| phone            | string, required without email. | The customer's phone number                                          |
| channels         | array                           | Include "email", "sms", or both channels.                            |
| reminders\_count | integer                         | 0 - 3 reminders.                                                     |
| asked\_at        | date                            | The date to schedule the request. If null, it will send immediately. |

#### Create a customer charge

<mark style="color:green;">`POST`</mark> `https://api.moregoodreviews.com/beacon/charges`

Records a charge for the customer. You must first create the customer before adding charges.

**Body**

<table data-full-width="false"><thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td>email</td><td>string, required without phone.</td><td>The customer's email address.</td></tr><tr><td>phone</td><td>string, required without email.</td><td>The customer's phone number.</td></tr><tr><td>amount</td><td>integer</td><td>Amount of charge in lowest currency denomination.</td></tr><tr><td>currency</td><td>string</td><td>The 3-letter currency code.</td></tr><tr><td>location_slug</td><td>string</td><td>The slug of a <a href="https://moregoodreviews.com/settings/locations">location</a>. If provided, the default location for the customer will be changed to this one.</td></tr><tr><td>charged_at</td><td>date</td><td>The date the customer was charged.</td></tr></tbody></table>

#### Get customers

<mark style="color:blue;">`GET`</mark> `https://api.moregoodreviews.com/beacon/customers`

Gets all customers for a project.

#### Get customer reviews

<mark style="color:blue;">`GET`</mark> `https://api.moregoodreviews.com/beacon/customers/:id/reviews`

Gets all reviews the customer submitted.

#### Get customer messages

<mark style="color:blue;">`GET`</mark> `https://api.moregoodreviews.com/beacon/customers/:id/messages`

Gets all messages sent to a customer.

#### Get reviews

<mark style="color:blue;">`GET`</mark> `https://api.moregoodreviews.com/beacon/reviews/`

Gets all reviews for a project.

#### Get messages

<mark style="color:blue;">`GET`</mark> `https://api.moregoodreviews.com/beacon/messages`

Get all messages sent for the project.

### Pagination

For requests that require pagination, a pagination key is added to the response. This key might look something like the following:

<pre class="language-json"><code class="lang-json">"pagination": {
<strong>  "current_page": 2,
</strong>  "path": "https://api.moregoodreviews.com/beacon/customers",
  "first_page_url": "https://api.moregoodreviews.com/beacon/customers?page=1",
  "last_page_url": "https://api.moregoodreviews.com/beacon/customers?page=3",
  "prev_page_url": "https://api.moregoodreviews.com/beacon/customers?page=1",
  "next_page_url": "https://api.moregoodreviews.com/beacon/customers?page=3",
  "from": 51,
  "to": 100,
  "total": 110,
  "per_page": 50,
  "last_page": 3
}
</code></pre>
