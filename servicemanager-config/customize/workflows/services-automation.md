# Services Automation

The Service Automation first takes the service that the request was raised under, and then updates the status of the services that are related to this service.

## Before you begin
* Read about [service dependancies](/servicemanager-user-guide/service-portfolio/services/service-dependancies).

![Services automation](/_books/servicemanager-config/images/workflow-services-status.png)

The service status can help both the support staff and users on the portals to identify when a service is impacted or unavailable. The changes in service status can also contribute to the service [availability metrics](/service-portfolio/services/service-availability#availability-metrics).

## Status task

#### Options
* **Request ID**. This is a mandatory option, but in most cases it should be set to `Auto`, which automatically picks up the request ID from the request that the workflow is running on.
* **Relationship Type**. This option sets the status update based on the dependency between the request's service and that service's dependencies. The default is set to `Ignore`, which will apply the status change to all services, independent of the dependency. The dependency options include:
    * Related and Request Service depend on each other
    * Request Service depends on Related
    * Related depends on Request Service
* **Status**. This is a mandatory option.  This needs to be set to `Manual` and then one of the available statuses needs to be selected.

:::tip
The related services do not need to be added as a related service on the request for the status to be updated.
:::
