---
description: Run your own reviews agency with the MGR white label.
icon: briefcase
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
---

# White Label

Onboard your own customers using your own white labeled version of the product. If you have upgraded to the agency plan, you will see an Agency button in the header of the console. From here, you can configure your agency, create new projects under your agency, and invite your clients to access one or more of your agency projects.

### Getting Started

It is important to configure all of the settings to get your agency up and running properly. This includes the following:

* Basic Info - Your agency name and other copy.
* Branding - Your logo, icon, and primary color.
* Meta - The title, description, and image to use for your meta data. This is what appears on your customer portal and console when visiting your custom domain name.
* Domain - There are several options for configuring your domain name. The most important are the domain for sending emails and the domain for your client portal. You can learn more about the domain setup process, [here](domain-setup.md).
* API - Your agency’s secret API key for integrations that use agency-level endpoints. You can copy or rotate the key on the [API](api.md) page, similar to a project API key.

### Adding Projects

Once you have set up your agency, you can go ahead and create your first project. When creating new projects under your agency, it is important you do that in the agency section, [here](https://moregoodreviews.com/agency/projects).

### Inviting Clients

A client will most likely have just one project. Once you set it up, you can invite them as a member of your agency with access to that one project. You can think of an agency like a "space". A space can have one or more projects. It can also have one or more members with access to one or more projects inside of it. An agency functions the same way. If you have configured your agency with a sending domain and client portal domain, the invite email to your client will come from your domain and link directly to your client portal domain for them to create an account.

### Sending Limits

Your account's request limit is shared across all of your projects, and thus all of your clients. You can throttle the requests on a project basis by going into each project's [strategy](https://moregoodreviews.com/settings/strategy#limits) and updating the daily and monthly request limits (for both email and SMS). This will allow you to divide up your requests evenly across all of your clients. If a limit is reached, we will wait until the following day or month to continue sending review requests.

### Billing Clients

We do not offer a billing solution for your clients. You will need to onboard and invoice them accordingly with a 3rd party invoicing system like [Stripe](https://stripe.com) or [Invoicely](https://invoicely.com/). It is up to you how much you would like to charge for the service.
