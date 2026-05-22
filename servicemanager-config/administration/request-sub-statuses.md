---
layout: article-toc
---
# Request Sub-statuses
The request sub-statuses lets you define a number of descriptive states of a request that are related to the request being either Active or On-hold. Using the Sub-status can help control the situations under which a request is put On-hold or made Active again. An example of an On-hold Sub-status might be With Customer which when selected could place the request's status to On-hold and stop any allocated Service Level Target timers.

:::note
The Sub-statuses defined here are global and will be visible to all the selected Request Types. Service based sub-statuses can be configured within the Service form for a particular service.
:::

## Managing Request Sub-statuses
The Management of the Global Request Sub-statuses is done from within the Administration Portal

* **Sub-status Name**<br>The Name of the sub-status is what will be displayed to an analyst from within a request.
* **Customer Label**<br>An alternative Label can be provided which will be visible to the customer from within the Customer or Service Portals. This is only applicable to request types that are accessible on the Portals.
* **Request Type**<br>A sub-status can be made available to All requests types or you can select from one of the available request types on which this particular Sub-status will be available.
* **Parent Status Active On-Hold**<br>The selection of a sub-status controls if the request is placed in either an Active or On-hold state when the sub-status is selected. A Sub-status that is set with a Parent Status of Active will either keep the request in an active state (New, Open, Resolved) or if the request is On-hold the state will change back to its Active state. A Sub-status that is set with a Parent Status of On-hold will either change the status of the request to On-hold if it is currently in an active state (New, Open, Resolve) or it will maintain an On-hold state if it is already on-hold.
* **Reason Required**<br>This setting is used to enforce an entry by the user that is putting the request on-hold for this particular sub-state.
* **Pause Until Date / Time**<br>If choosing the Parent Status of On-Hold, this option will allow you to determine if the analyst moving the request into a specific sub-status will be prompted to put it on-hold until a defined date and time, after which it will automatically come off-hold, or if you choose No the analyst will not be prompted to set an on-hold until date and time, and instead the request will remain on-hold until it is manually taken off-hold. If choosing this option the analyst will be presented with the option to set a reminder activity when placing the request into this on-hold status.
Information When creating your sub-statuses it is important that at least one Active sub-status exists to allow you to move from an On-hold state to an Active state.
* **Language**<br>If you support more than one language in your environment you can provide the appropriate translations for these languages
* **Status**<br>Only Sub-statuses set to Published will be visible to use in Service Manager.
    * **Draft**<br>Can be used to create Sub-statuses but not be visible.
    * **Retired**<br>Once Published, a Sub-status can be moved into a retired status if no longer required.
* **Auto-Update**<br>Toggle this option On If you wish to allow customer updates (Portal or Email) to a request whilst in this Sub-Status, to automatically change the Sub-status, to the Sub-Status defined in the On Customer Update change the Sub-Status to... dropdown, on the Service and Request Type of the Request.

:::tip
 The Sub-Status which a customer update will change to, can be configured per service and per request type on the Service views in Service Manager, making this granular per Service and Request Type.
:::

## Notifications
Use the Following System Settings to control if teams or owners receive notifications if the Sub-statuses are changed:

|Setting|Description|
|-|-|
|guest.app.requests.notification.notificationType.subStatusChange|Choose if the Owner should receive No notification Email Only, Hornbill Only, Both|
|guest.app.requests.notification.notificationType.subStatusChangeTeam|Choose if the Members of the Team owning a request should receive No notification, Email Only, Hornbill Only, Both|

If Choosing Email as a notification option, specify which email template will be sent, using the following system settings:

|Setting|Description|
|-|-|
|guest.app.requests.notification.emailTemplate.analystSubStatusUpdate|The email template to be used when sending an email analyst sub-status update notification|
|guest.app.requests.notification.emailTemplate.groupSubStatusUpdate|The email template to be used when sending an email group sub-status update notification|

<!-- https://wiki.hornbill.com/index.php?title=Global_Request_Sub-statuses>