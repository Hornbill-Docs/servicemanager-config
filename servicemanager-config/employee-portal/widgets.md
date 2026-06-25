# Employee Portal widgets

With Service Manager installed, there are several Employee Portal widgets that are included to enhance the user's experience with information and tools specific to Service Manager.

## Before you begin

* Be familiar with [designing the Employee Portal](/esp-config/customize/employee-portal/employee-portal-design).
* See the list of [general widgets](/esp-config/customize/employee-portal/employee-portal-widgets).

## Accessing the Service Manager widgets

1. View the Employee Portal using the **My Company** menu item under the **Home** option in the left-hand vertical menu bar.
1. Navigate to the [page](/esp-config/customize/employee-portal/employee-portal-design#page-details) where the Service Manager widget will be added.
1. Enter **Design Mode**.
1. Expand the **Add Widgets** section in the right-hand Page Details panel.
1. Select **Service Manager** from the dropdown of available apps.

![Add Service Manager Widgets](/_books/servicemanager-config/images/ep-add-widgets.png)

## Average Rating widget

The average [star rating](/servicemanager-user-guide/service-portfolio/customer-feedback) widget collects data from all of the requests from all services and displays an average overall rating. These requests will have been closed and the customers will have provided a star rating.

![Average Rating](/_books/servicemanager-config/images/ep-rating-widget.png)

### Configure

* **Filter by Service Domain.**  If the widget is being placed on a page for a specific [domain](/esp-config/customize/service-domains), you can add the domain name to show only the average feedback for that domain.
* **Last X days.** By default, the widget will show the average for all historical feedback.  Optionally you can select 30, 60, 90, or 120 days of data to be displayed. The selected number of days will be displayed in the widget.

:::tip
This widget is best displayed using a single column.
:::

## Service Availability widget

The [service availabilty](/servicemanager-user-guide/service-portfolio/services/service-availability) widget collects data from the selected service and displays the availability over the previous X number of days.

![Service Availability](/_books/servicemanager-config/images/ep-service-availability-widget.png)

### Configure

* **Service ID.**  You must add a service ID for the widget to show any information. Only one service can be displayed per widget.  
* **Last X days.** By default, the widget will show all the historical availability data.  Optionally you can select 30, 60, 90, or 120 days of data to be displayed. The selected number of days will be displayed in the widget.

:::tip
This widget is best displayed using a single column.
:::

## Requests widget

The Requests widget provides a list of requests that have been raised either by the user or for the user.  In addition to their requests, users can view requests they are connected with, or requests that their managed staff have raised.

![Request Widget](/_books/servicemanager-config/images/ep-requests-widget.png)

## Search widget

The Search widget provides a unified search for users to find information on services, FAQs, service requests, known issues, the user's active requests, and knowledge articles.

![Search Widget](/_books/servicemanager-config/images/ep-search-widget.png)

### Configure

* **Filter by Service Domain.** Select a single service domain that the search will apply to.  
* **Filter by Types.** You can limit the search to only selected types of records.
  * Service
  * FAQ
  * Service Request
  * Known Issues
  * My Service Requests
  * Articles

## Knowledge base articles

This widget presents a list of knowledge base articles that are available to the user. A search and knowledge base filter allows the user to find a particular article. The search is based on the article's name.  Clicking on an article in the list will open the full article in the Knowledge browser.

![Knowledge Article Widget](/_books/servicemanager-config/images/ep-knowledge-article-widget.png)

### Configure

* **Knowledge Bases.** From the list, select which knowledge bases will be included when searched.
* **Knowledge Base Article Types**. From the list, select which knowledge types can be used to control the types of knowledge articles that will be searched.

## My Assets Widget

The My Assets widget is an Employee Portal widget that gives users a quick view of assets that they use.

![My Assets Widget](/_books/servicemanager-config/employee-portal/images/my-assets-widget.png)

|Purpose|Default behavior|Configuration|
|---|---|---|
|Show users the assets they use or assets that have been shared with them.|The widget automatically uses the signed-in user. The user cannot change this to view another person's assets.|Administrators can choose which additional asset details appear on each card.|

### What assets are shown

The widget shows assets related to the signed-in Employee Portal user using this scope:

|Relationship|Shown in the widget?|Meaning|
|---|---|---|
|Used By|Yes|The asset is assigned to the user as the person using it.|
|Shared With|Yes|The asset is shared directly with the user or shared with a group the user belongs to.|
|Owned By|No|The widget does not include assets where the user is only set as the owner.|
|Archived assets|No|Archived assets are excluded from the default Employee Portal widget view.|

### Number of assets

* If the user has 12 or fewer matching assets, the widget shows the asset cards directly without search, sort, or result count. This keeps the widget simple for small lists.
* If the user has more than 12 matching assets, the widget shows search, order options, result count, and pagination.

### Searching and Ordering

* Search is available for larger lists. Leading and trailing spaces are trimmed before the search request is sent.
* Users can order by name, created date, or updated date. Ascending and descending arrows are available in the order menu.

### Asset links, images, and icons

* Asset names are links only for users with the relevant Asset Management view or administration rights. Other users see asset names as text.
* The widget shows uploaded asset images where available. If an image is unavailable, it falls back to the asset class icon.
