---
layout: article-toc
---
# Simple Lists

The Simple Lists provide a way to define different pick lists or combo-box selections that are used through out the Service Manager app. The available options in a pick list or combo-box can also be translated into different languages from within the Simple List editor.

## Service Manager Simple Lists

A number of Simple Lists are installed with Service Manager.  

|List Name|Description|
|-|-|
|bpmAuthorisationType|This list is used in conjunction with the "Auto Assign Authorization" business process nodes. The authorization types specified in this list are relied upon by the underlying operation|
|bpmBoolean|Used in conjunction with many Service Manager business process operations which require a "Yes" or "No" for options in automated tasks (e.g. Shown when choosing whether to include a System Timeline Update, an option supported by various automated operations).|
|bpmRequestAction|Used to display the list of the available Action Tabs in a Request. This is used in conjunction with the Service Manager Suspend operations when setting the "Action Focus" option.|
|bpmRequestConnections|This list is used in conjunction with the Connection-related business process operations. When adding or emailing the connections of a request via the corresponding business process operations, the Connection type is specified and takes the values from this list. The Connection types specified in this list are relied upon by the underlying operation and therefore the existing values should not be changed or any new values added.|
|bpmRequestResolveAction|Used to supply the values "Resolve" and "Close" in the business process operation "Resolve Linked Requests".|
|bpmRequestStatus|This list is used in conjunction with various Service Manager business process operations which use status values. E.g. the operations "Update Request Status" or "Suspend Wait for Status Change". The request statuses specified in this list are relied upon by the underlying operation and therefore the existing values should not be changed or any new values added.|
|bpmRequestTimelineVisibility|This list is used in conjunction with various Service Manager business process operations which add a timeline update as part of their operation. The timeline update can have a visibility level applied which governs who can see that particular update. The timeline visibility levels specified in this list are relied upon by the underlying operation and therefore the existing values should not be changed or any new values added.|
|bpmRequestType|Used to display a list of the available Request types in Service Manager. This is used when configuring the "Request Type" option in the "Resolve Linked Requests" business process operation.|
|CancellationReasons|This list supplies the Cancellation reasons that are available when a request is canceled using the corresponding "Cancel" request action button. Items can be added or removed from this list to suit your requirements.|
|changeCategory|This list provides the typical Change Categories "Major", "Minor", and "Significant". . Currently, this is not tied to any existing form or menu and can be used at your convenience to support any Intelligent Capture custom form you create.|
|changeRequestType|This list supplies the values found on the "Change Type" Intelligent Capture form. Items can be added or removed from this list to suit your requirements.|
|integrationJiraIssueType||
|integrationJiraProjectName||
|releaseCategory|This list provides the release categories "Major", "Minor", and "Significant". Currently, this is not tied to any existing form or menu and can be used at your convenience to support any Intelligent Capture custom form you create.|
|releaseRequestType|This list supplies the values found on the "Release Type" Intelligent Capture form. Items can be added or removed from this list to suit your requirements.
|Report Categories|This list is used in conjunction with Service Manager In-App reporting (a feature currently in development). It supplies the different categories used to sort the various Service Manager Reports that will be shipped with the feature. The Report Categories specified in this list are relied upon by the Service Manager Application and therefore the existing values should not be changed or any new values added.|
|Report Table Headings|This list is used in conjunction with Service Manager In-App reporting (a feature currently in development). It lists the currently available column headings that can be displayed within the in-app reports shipped with the feature. The Report column headings specified in this list are relied upon by the Service Manager Application and therefore the existing values should not be changed or any new values added.|
|Reports|This list is used in conjunction with Service Manager In-App reporting (a feature currently in development). It lists the currently available in-app reports that will be shipped with the feature. The Report names specified in this list are relied upon by the Service Manager Application and therefore the existing values should not be changed or any new values added.
|requestConnectionType|When adding a connection to a request either via the Connection action button within the request or via a business process operation it is necessary to specify a connection type. This list supplies the available values. The connection types specified in this list are relied upon by the Service Manager Application and therefore the existing values should not be changed or any new values added.|
|serviceCategory|The service category is a list of values that can used to help organize the services you create. Service categories are simply a way of grouping or classifying Services. Items can be added or removed from this list to suit your requirements.|
|serviceStatus|Contains the Service Status values used to manage the services within the Service Portfolio. The status values specified in this list are relied upon by the Service Manager Application and therefore the existing values should not be changed or any new values added.|
