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

#### Customers

<details>

<summary><mark style="color:$warning;"><code>POST</code></mark>  Create or update a customer</summary>

<mark style="color:$warning;">`POST`</mark> `https://api.moregoodreviews.com/beacon/customers`

Creates a new customer or updates an existing one.

**Body**

<table data-full-width="false"><thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td>first_name*</td><td>string</td><td>The customer's first name.</td></tr><tr><td>last_name</td><td>string</td><td>The customer's last name.</td></tr><tr><td>email</td><td>string</td><td>The customer's email address.</td></tr><tr><td>phone</td><td>string</td><td>The customer's phone number.</td></tr><tr><td>company</td><td>string</td><td>The customer's company name.</td></tr><tr><td>has_subscription</td><td>boolean</td><td>Whether or not the customer is subscribed to your service.</td></tr><tr><td>location_slug</td><td>string</td><td>The slug of a <a href="https://moregoodreviews.com/settings/locations">location</a>.</td></tr><tr><td>signed_up_at</td><td>date</td><td>The date the customer signed up to your service.</td></tr></tbody></table>

</details>

<details>

<summary><mark style="color:$warning;"><code>POST</code></mark>  Create a customer charge</summary>

<mark style="color:$warning;">`POST`</mark> `https://api.moregoodreviews.com/beacon/charges`

Records a charge for the customer. You must first create the customer before adding charges.

**Body**

<table data-full-width="false"><thead><tr><th>Name</th><th>Type</th><th>Description</th></tr></thead><tbody><tr><td>email</td><td>string, required without phone.</td><td>The customer's email address.</td></tr><tr><td>phone</td><td>string, required without email.</td><td>The customer's phone number.</td></tr><tr><td>amount</td><td>integer</td><td>Amount of charge in lowest currency denomination.</td></tr><tr><td>currency</td><td>string</td><td>The 3-letter currency code.</td></tr><tr><td>location_slug</td><td>string</td><td>The slug of a <a href="https://moregoodreviews.com/settings/locations">location</a>. If provided, the default location for the customer will be changed to this one.</td></tr><tr><td>charged_at</td><td>date</td><td>The date the customer was charged.</td></tr></tbody></table>

</details>

<details>

<summary><mark style="color:$success;"><code>GET</code></mark>  Get customers</summary>

<mark style="color:$success;">`GET`</mark> `https://api.moregoodreviews.com/beacon/customers`

Gets all customers for a project.

</details>

<details>

<summary><mark style="color:$success;"><code>GET</code></mark>  Get customer reviews</summary>

<mark style="color:$success;">`GET`</mark> `https://api.moregoodreviews.com/beacon/customers/:id/reviews`

Gets all reviews the customer submitted.

</details>

<details>

<summary><mark style="color:$success;"><code>GET</code></mark>  Get customer messages</summary>

<mark style="color:$success;">`GET`</mark> `https://api.moregoodreviews.com/beacon/customers/:id/messages`

Gets all messages sent to a customer.

</details>

#### Reviews

<details>

<summary><mark style="color:$warning;"><code>POST</code></mark>  Create a review request</summary>

<mark style="color:$warning;">`POST`</mark> `https://api.moregoodreviews.com/beacon/asks`

Schedules a review request for the customer.

**Body**

| Name             | Type                            | Description                                                          |
| ---------------- | ------------------------------- | -------------------------------------------------------------------- |
| email            | string, required without phone. | The customer's email address                                         |
| phone            | string, required without email. | The customer's phone number                                          |
| channels         | array                           | Include "email", "sms", or both channels.                            |
| reminders\_count | integer                         | 0 - 3 reminders.                                                     |
| asked\_at        | date                            | The date to schedule the request. If null, it will send immediately. |

</details>

<details>

<summary><mark style="color:$success;"><code>GET</code></mark>  Get reviews</summary>

<mark style="color:$success;">`GET`</mark> `https://api.moregoodreviews.com/beacon/reviews/`

Gets all reviews for a project.

</details>

#### Locations

<details>

<summary><mark style="color:$warning;"><code>POST</code></mark>  Create a location</summary>

<mark style="color:$warning;">`POST`</mark> `https://api.moregoodreviews.com/beacon/locations`

Creates a location for a project.

**Body**

| Name          | Type   | Description                                                    |
| ------------- | ------ | -------------------------------------------------------------- |
| name\*        | string | The name of the location.                                      |
| display\_name | string | The customer-facing name for the location. Falls back to name. |
| slug          | string | The slug for the location. Generated if left out.              |
| code          | string | An optional store code.                                        |
| address1      | string | Address line 1.                                                |
| address2      | string | Address line 2.                                                |
| city          | string | The city or town.                                              |
| state         | string | The state or region.                                           |
| zip           | string | The postal code.                                               |

</details>

<details>

<summary><mark style="color:$primary;"><code>PUT</code></mark>  Update a location</summary>

<mark style="color:$primary;">`PUT`</mark> `https://api.moregoodreviews.com/beacon/locations/:id`

Updates a location.

**Body**

| Name          | Type   | Description                                                    |
| ------------- | ------ | -------------------------------------------------------------- |
| name          | string | The name of the location.                                      |
| display\_name | string | The customer-facing name for the location. Falls back to name. |
| slug          | string | The slug for the location. Generated if left out.              |
| code          | string | An optional store code.                                        |
| address1      | string | Address line 1.                                                |
| address2      | string | Address line 2.                                                |
| city          | string | The city or town.                                              |
| state         | string | The state or region.                                           |
| zip           | string | The postal code.                                               |

</details>

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
