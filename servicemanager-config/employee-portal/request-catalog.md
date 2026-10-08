---
layout: article-toc
---

# Request Catalog

The Request Catalog is an Employee Portal page that brings together all the types of request a user can raise in one place. Users don't have to open each service in turn to find the type of request that they want to raise. They can browse or search everything from a single page.

![Request Catalog](/_books/servicemanager-config/employee-portal/images/request-catalog.png)

## Before you begin

* **Enabling the Request Catalog**: The Request Catalog is disabled by default. You must [enable it](#how-to-enable-the-request-catalog) before it can be used.
* **Employee Portal design**: The **Employee Portal Manager** role is required to add a Links widget.

## How to enable the Request Catalog

1. Open [Configuration](/esp-config/getting-started/using-configuration) and select `Service Manager`.
2. Select `Application Settings`.
3. Search for `guest.app.selfService.requestCatalog.enabled`.
4. Set the value to **On**.

## How to provide access to the Request Catalog

Once enabled, your Request Catalog is available at the URL: `https://live.hornbill.com/<your-instance-id>/servicemanager/selfservice/requestcatalog`.

### Links widget

Using the [Links widget](/esp-config/customize/employee-portal/employee-portal-widgets#links-widget), you can add the Request Catalog to your Employee Portal.

![Request Catalog Link Widget](/_books/servicemanager-config/employee-portal/images/request-catalog-link-widget.png)

1. Open the Employee Portal and enter Design Mode.
1. Add a Links widget to the page.
1. Add a new link to the widget, and set the link's URL to the Request Catalog URL.
1. Set the link's name to something like "Request Catalog" and optionally add an icon.
1. Save the widget and publish the changes, then exit Design Mode.

### Sharing the Request Catalog URL

You can provide users with the direct link to the Request Catalog by sharing the URL. This might be through email, LIVE Chat, or other communication channels.

## User features

### Filters

* **All requests**: Displays every type of request that the user can make. This will only include request items from services that they are subscribed to.

#### Quick access

* **Recently used**: Displays the request items that the user has raised in the last 90 days. This will not be available if the user has not raised any requests.
* **Popular items**: Displays the most popular request items over the last 90 days across the services that the user is subscribed to.

#### Services, service categories, and service domains

Only one of these filters can be enabled at a time. Select the filter that best suits your users or how you have your services structured.

* **Services**: Displays the services that the user is subscribed to. Selecting a service will show only the request items for that service.
* **Service categories**: Displays the service categories based on the services that the user is subscribed to. Selecting a service category will show the request items for all the services under that category.
* **Service domains**: Displays the domains that the user has access to. Selecting a domain will show the request items for all the services under that domain.

|Setting|Description|Default|
|---|---|---|
|guest.app.selfService.requestCatalog.viewMode|Controls which filter is available to users. Options are: `services`, `serviceCategories`, or `serviceDomains`.|`services`|

## Request view options

* **Search Request Catalog**: Users can search for request items by entering keywords in the search box. The search will look for matches in the Title and Description of request items.
* **Sort by**: Users can sort the request items alphabetically or by popularity.
* **List view**: Shows a list of request items, with the columns Title, Service, and Description. Clicking anywhere in a row will start the process of raising the request.
* **Card view**: Shows a card for each request item, with the Title, Service, and Description. Clicking anywhere in a card will start the process of raising the request.

> **Tip:** The Request Catalog uses the names and descriptions you've set on your catalog items. Clear, task-based names (such as *Request remote access* rather than *Remote Access*) and descriptions that add detail beyond the name make it much easier for users to choose the right item. Consider how clear the catalog item names and descriptions are when they are viewed alongside items from other services.
