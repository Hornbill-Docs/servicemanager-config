---
layout: article-toc
---
# Scheduled Requests
The Scheduled Requests feature enables Service Manager requests to be generated automatically with a predetermined timetable.  For instance, there may be a need to schedule a change to your environment to happen on a weekly or monthly basis.

## Topics covered
* Accessing the Scheduled Requests view
* Creating a scheduled request
* Reactivating an expired scheduled request
* Viewing the Schedule calendar

## Before you begin
* You must have either the Service Desk Admin or the Hornbill Admin role.

## How to access
**To get to the Scheduled Requests view:**
1. Open [Configuration](/esp-config/getting-started/using-configuration) and search for *Scheduled Requests*.
1. Select **Scheduled Requests** from the results list.

*or*

1. Navigate to **[Configuration](/esp-config/getting-started/using-configuration) > Service Manager > Administration > Scheduled Requests**.

## Adding a scheduled request
**To create a scheduled request:**
1. In the Scheduled Requests list, click **Create New** (the plus icon).
1. Complete the fields described in [Details](/servicemanager-config/administration/scheduled-requests#details).
1. (Optional) Click **Assets** (the monitor icon) to go to the Assets tab; search to associate one or more assets.
1. Click the clock icon to go to the Scheduling tab; set up a schedule as described in [Scheduling tab](/servicemanager-config/administration/scheduled-requests#scheduling-tab).
1. Click **Create**.

### Details
* **Name.** (Required) Give the scheduled request a name that is unique to other scheduled requests. This field sets the summary field of the request.
* **Description.** This information is added to the Description field of the request.
* **Request Type.** (Required) The available request types for scheduling are Incident, Service Request, and Change. 
    :::tip
    Make sure the request type you choose is enabled and configured on the selected service.
    :::
* **Service.** This dropdown shows the services that the current user supports. Select the service that the request will be associated with.
* **Catalog.** Select the request catalog item that the request will be associated with. 
    :::note
    As this is an automated scheduled request, the Intelligent Capture associated to this request catalog item will not be used to capture information.
    :::
* **Team.** Select the team that this request will be assigned to.  Make sure this team supports the selected service.

### Scheduling tab
In the Scheduling tab, you can set a schedule for the request by specifying things such as its recurrence, when it first runs, which days or months it runs, and when it expires.

**Recurrence Pattern.** Select one of the following scheduling options:
* Run Once
* Run Daily
* Run Monthly
    ::: note
    When scheduling monthly, make sure that the selected day is valid for every month that the job will run.
    ::: 
* Run Every Period

**Next Event Date.** This is where you set the date and time for when the first event will take place.  Once the first event has happened, this field will display the date and time of the next scheduled event.

**Expire Count.** (Not applicable to the **Run Once** option.)  This limits the number of times the scheduled request will run.  Independent of how many days or months are selected in the schedule, a scheduled request stops once this number has been reached. 
Use `-1` if you don't want to limit the number of times that the scheduled request is run.

## Reactivating an expired scheduled request
After a scheduled request has been completed and there are no more recurrences to create a new request, the status is changed to *Expired*.  

**To reuse an expired scheduled request:**
1. In the list of scheduled requests, click **Update** (the pencil icon) on the expired scheduled request that you want to reactivate.
1. Click the clock icon to go to the Scheduling tab.
1. (Optional) Update the schedule.
1. Click **Reactivate**.

## Viewing the Schedule calendar
You can view all scheduled requests in a calendar view. For each scheduled request, the initial logged request along with its next scheduled event will be displayed in the calendar.

**To access the calendar:**
1. At the top of the Scheduled Requests view, click **Schedule Calendar** (the calendar icon).
1. (Optional) Use the **Select scheduled request** dropdown to limit the calendar view to a single scheduled request.