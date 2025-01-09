---
layout: article-toc
keywords: progressive capture,app.itsm.progressiveCapture.new
---
# Using Intelligent Capture
Intelligent Capture allows you to configure what information is collected or captured when a request is being manually raised. This may consist of a single question or a collection of questions that are presented to a user. The captured information can help with the fulfillment of the request.  
<br>
![Capture Question](/_books/servicemanager-config/customize/images/portal-custom-capture-question.png)

Intelligent Capture scripts are initiated from the different locations where a new request can be raised. This might be a support person raising a new request from their request list or a customer raising a request on a self-service portal.


## Topics Covered
* Where Intelligent Capture scripts are used.
* Advanced settings.

## Before You Begin
* Know how to search for settings in [Configuration](/esp-config/getting-started/using-configuration).

## Request List
When raising a request from the [Request List](/servicemanager-user-guide/request-list/overview/), a capture script can be used to help guide the user through the collection of information that is required to submit the new request. 

The `Raise New` option, located at the top right of the Request List, is split into two functional areas.

![Raise New Request](/_books/servicemanager-config/customize/images/raise-new-request-button.png)

* **Raise New**<br>Clicking on the main button labeled `Raise New` will initiate an Intelligent Capture that is not specific to any request type. When the service desk receives a phone call, they can click on this button to immediately follow a capture script that presents them with questions to help determine the type of request and who it should be assigned to. The `Raise New` button uses the capture that is specified in the following setting: 
    * **New Request**<br>app.itsm.progressiveCapture.newRequest
* **Request Types**<br>Clicking on the down-arrow shows a list of available request types that the user has the right to raise. These can be used when a user knows the type of request that they want to raise. Specify the Intelligent Capture for each request type using its associated setting:
    * **New Incident**<br>app.itsm.progressiveCapture.newIncident
    * **New Service Request**<br>app.itsm.progressiveCapture.newServiceRequest
    * **New Problem**<br>app.itsm.progressiveCapture.newProblem
    * **New Known Error**<br>app.itsm.progressiveCapture.newKnownError
    * **New Change**<br>app.itsm.progressiveCapture.newChange
    * **New Release**<br>app.itsm.progressiveCapture.newRelease

The `Raise New` button can also be configured to only show one of the above options. This can be helpful in reducing the overhead of managing multiple Intelligent Capture scripts.
* **Hide**<br>Turn the setting *app.request.raiseNew.hide* to `ON` to hide the generic `Raise New` option and always have the user select a specific request type. Individual Intelligent Captures can be managed for each request type and remove the need to manage a generic Intelligent Capture script for the `Raise New` option.
* **Limit**<br>Turn the setting *app.request.raiseNew.limit* to `ON` to only allow the `Raise New` option and remove the ability for a user to select a specific request type. This removes the need to manage multiple Intelligent Capture scripts per request type. The request type can be determined by using the [Request Type form](/service-manager-config/customize/service-manager-capture-forms#release-type) or by selecting a Request Catalog Item on the [Services form](/service-manager-config/customize/service-manager-capture-forms#services).  

## Email
From the Email View, a new request can be manually raised from an email. Clicking on `Raise Request` from the `More` button will by default initiate the Intelligent Capture specified in the *app.itsm.progressiveCapture.newRequest* setting. This is the same capture used by the `Raise New` button on the request list.

![Raise Request](/_books/servicemanager-config/customize/images/raise-request-from-email.png)
:::tip
If you need an alternative capture script when raising requests from an email, use the setting *app.itsm.progressiveCapture.newRequestFromEmail* to specify the capture script to use.
:::

## Employee and Customer Portals
Each service that is available to a user or contact on the portals has a [request catalog](/servicemanager-user-guide/service-portfolio/request-catalog) that can include several request models.  Each request model can have an associated Intelligent Capture that is used to collect information specific to that request.

![Request Model](/_books/servicemanager-config/customize/images/request-model-capture.png)

:::tip
Some capture forms are hidden from users on the portals.  For example, the [Services Form](/servicemanager-config/customize/service-manager-capture-forms#services) is not presented to the user because they are already raising the request from the Service and this is automatically captured. See the [Service Manager Forms](/servicemanager-config/customize/service-manager-capture-forms) documentation for more information on the visibility of each individual form.
:::