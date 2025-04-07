# Employee Portal widgets
With Service Manager installed, there are serveral Employee Portal widgets that are included to enhance the user's experience with Service Manager specific information and tools.

## Before you begin
* Be familiar with [designing the Employee Portal](/esp-config/customize/employee-portal/employee-portal-design).
* See the list of [general widgets](/esp-config/customize/employee-portal/employee-portal-widgets).

## Accessing the Service Manager widgets
1. View the Employee Portal using the **My Company** menu item under the **Home** option in the left-hand verticle menu bar.
1. Navigate to the page where the Service Manager widget will be added.
1. Enter **Design Mode**.
1. Expand the **Add Widgets** section in the right hand Page Details panel.
1. Select **Service Manager** from the dropdown of available apps.

![Add Service Manager Widgets](/_books/servicemanager-config/images/ep-add-widgets.png)

## Average Rating
The average [star rating](/servicemanager-user-guide/service-portfolio/customer-feedback) widget collects data from all of the requests from all services and displays an average overall rating. These requests will have been closed and the customers will have provided a star rating.

![Average Rating](/_books/servicemanager-config/images/ep-rating-widget.png)

### Configure

* **Filter by Service Domain**.  If the widget is being placed on a page for a specific [domain](/esp-config/customize/service-domains), you can add the domain name to only show the average feedback for that domain.
* **Last X days**. By default, the widget will show the average for all historical feedback.  Optionally you can select 30, 60, 90, or 120 days of data to be displayed. The selected number of days will be displayed in the widget.

:::tip
This widget is best displayed using a single column.
:::

## Requests
The Requests widget provides a list of requests that have been raised either by the user or for the user.  In addition to their requests, there are options to view requests that they are connected with, or requests that their managed staff have raised.

![Request Widget](/_books/servicemanager-config/images/ep-requests-widget.png)

## Search
The Search widget provides a unified search for users to find information on services, FAQs, service requests, known issues, the user's active requests, and knowledge articles.

![Search Widget](/_books/servicemanager-config/images/ep-search-widget.png)

### Configure
* **Filter by Service Domain**. Select a single service domain that the search will apply to.  
* **Filter by Types**. The search can be limited to only searching selected types of records.
    * Service
    * FAQ
    * Service Request
    * Known Issues
    * My Service Requests
    * Articles

## Knowledge base articles
This widget presents a list of knowledge base articles that are available to the user. A search and knowledge base filter allows the user to find a particular article. The search is based on the article's name.  Clicking on an article in the list will open the full article in the Knowledge Browser. 

![Knowledge Article Widget](/_books/servicemanager-config/images/ep-knowledge-article-widget.png)

### Configure
* **Knowledge Bases**. A list of selectable knowledges allows you to select which knowledge bases will be included when searched.
* **Knowledge Base Article Types**.  A list of selectable knowledge types can be used to control the types of knowledge articles that will be searched.
