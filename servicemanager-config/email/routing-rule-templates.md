---
layout: article-toc
---
# Routing Rule Templates

The routing rule templates provide a way to define default settings for requests that are automatically raised from emails using the [routing rules](/esp-config/email/using-email-routing-rules). An unlimited number of routing rule templates can be created. Each email routing rule can link to a single routing rule template. A single routing rule template can be used by multiple email routing rules.

![Routing Rule Template](/_books/servicemanager-config/images/routing-rule-template.png)

## Template options

Each template provides a number of options to define the default settings for the requests that are raised from an email routing rule.

* **Name**: The name is used for both providing a reference in the list of routing rule templates and for selecting the routing rule template when defining an email routing rule when the **Raise new request** operation is used.
* **Description**: An optional description of the routing rule template can be provided to help others that have access to this list understand the purpose of the template.
* **Request Type**: Available request types include incident and service request. This is a mandatory option. The selected option will result in that type of request being raised.
* **Service**: All the defined services that have a status of catalog are available within this list. Despite this being an optional field, using services is highly recommended.
* **Catalog Item**: The catalog item option is only available if a service has been selected and that service has available request catalog items
* **Team**: Select a team that this request will be assigned to. Keep in mind that a [workflow](/servicemanager-config/customize/workflows/using-workflows-with-service-manager) can also be used for automating the team assignments. If a service has not been selected, all teams will be available to select from. If a service has been selected in the service field, only the teams that support that service will be available.
* **Priority**: Allows for the initial priority to be set for the request. Keep in mind that the a workflow can also be used for automating the priority.
* **Assets**: One or more assets can be selected. These assets will be associated to the request and available within the assets section of the request.
* **Add Attachments**: This option determines whether attachments sent on an incoming email are added to the request as attachments for display within the request's **Attachments** section.

## Routing rule operations

Service Manager provides a number of [routing rule](/esp-config/email/using-email-routing-rules) operations that can be selected when configuring the system email routing rules. The routing rule templates are only available to the **Raise new request** operation.

![Routing Rule Operations](/_books/servicemanager-config/images/routing-rule-operations.png)

* **Raise new request**: This operation must be used if you wish to use the routing rule templates. When this operation is selected on an Email Routing Rule, an option is made available to select the Routing Rule Template that you wish to use when that Email Routing Rule is met.
* **Update request**: This operation does not use routing rule templates. This uses the default application settings to set the requests' initial settings
* **Log or update an existing incident**: This operation does not use routing rule templates. This uses the default application settings to set the requests' initial settings
* **Log or update an existing service request**: This operation does not use routing rule templates. This uses the default application settings to set the requests' initial settings

## Attachments

Attachments can be automatically added to the request attachments section using the following operations.

* **Raise new request**: When this operation is selected on an email routing rule, the option to enable/disable the adding of attachments is available on the routing rule template that you wish to use when that email routing rule is met.
* **Update request**: This operation does not use routing rule templates. This uses four [application settings](/servicemanager-config/advanced-tools-and-settings/application-settings) to control the adding of attachments for incidents, service requests, changes and problem records
  * `app.email.routing.rules.update.addAttachments.IN`
  * `app.email.routing.rules.update.addAttachments.SR`
  * `app.email.routing.rules.update.addAttachments.CH`
  * `app.email.routing.rules.update.addAttachments.PM`
