---
layout: article-toc
---
# Releases
Use the Releases automation at any stage in a workflow to automate release specific actions. These actions are only available to the releases entity.  

While the majority of automations for a release can use the standard request entity, there are a few unique values that are only available to releases that require the use of these automations.

## Suspend
Suspend automations will pause the workflow until a selected action is completed. 

### Available tasks
* **Wait for Release Type**<br>Use this Hornbill Automation to suspend the Business Process until a Release Type has been set on the Release record.
* **Wait for Request Schedule**<br>Use this node to pause the process and await the scheduling of the Release in the Change Calendar.

## Update Request
The Update Request automation is used to update values on a release record.

![Update Release Calendar](/_books/servicemanager-config/images/workflow-releases-update-calendar.png)

### Available tasks
* **Add to Change Calendar**<br>Use this task to automatically add the release record to the Change Calendar. Adding a release to the change calendar involves updating the release's schedule. This includes an option to enforce freeze periods to make sure releases are not scheduled during a [freeze period](/servicemanager-user-guide/change-calendar/overview#change-freeze-periods).  The schedule can also be added manually using the [Schedule Action](/servicemanager-user-guide/service-portfolio/requests/schedule-action) on the release record. 
* **Remove from Change Calendar**<br>Use this task to automatically remove the release from the change calendar. This will clear the date values that have been added to the [Schedule Action](/servicemanager-user-guide/service-portfolio/requests/schedule-action).
* **Release Type**<br>Use this task to update the Release Type. The Release Type is a field that is available only on release records. The default types include Emergency, Normal, and Standard.  These values are stored in a [Simple List](/servicemanager-config/setup/service-manager-simple-lists) called `releaseRequestType` that can be modified as needed.  

<!-- https://wiki.hornbill.com/index.php?title=Service_Manager_Business_Process_Workflow -->