---
layout: article-toc
---
# Scheduled Requests
The Scheduled Requests feature enables Service Manager requests to be generated automatically with a predetermined timetable.  For instance, there may be a need to schedule a change to your environment to happen on a weekly or monthly basis.

## Topics covered
* Accessing Scheduled Requests.
* Creating a scheduled request.
* Reactivating an expired scheduled request.

## Before you begin
* You must have either the Service Desk Admin or the Hornbill Admin role.

## Accessing
1. Open [Configuration](/esp-config/getting-started/using-configuration) and search for *Scheduled Requests*.
1. Select **Scheduled Requests** from the results list.

*or*

1. Navigate to **[Configuration](/esp-config/getting-started/using-configuration) > Service Manager > Administration > Scheduled Requests**.

## Adding a Scheduled Request

### Details
* **Name.** (Mandatory) Must be unique in name to other scheduled requests.  This field is also used to set the summary field of the request.
* **Description.** This information is added to the description field of the scheduled request.
* **Request Type.** The available request types for scheduling are Incident, Service Request, and Change. 
    :::tip
    Make sure the request type you choose is enabled and configured on the service.
    :::
* **Service.** This field will show the services that the current user supports. Select the service that the scheduled request will be associated with.
* **Catalog.** Select the  request catalog item that will be associated to this request.  
    :::note
    As this is an automated scheduled request, the Intelligent Capture associated to this request catalog item will not be used to capture information.
    :::
* **Team.** The team that this request will be assigned to.  Make sure this team supports the selected service.

### Assets
One or more assets can be associated to the scheduled request.

### Scheduling
#### Recurrence pattern
Select one of the following scheduling options
* Run Once
* Run Daily
* Run Monthly
    ::: note
    When scheduling monthly, make sure that the selected day is valid for every month that the job will run.
    ::: 
* Run Every Period

#### Next event date
When first creating a scheduled request, set the date and time for when the first event will take place.  Once the first event has happened, this field will display the date and time of the next scheduled event.

#### Expiry Count
All but the **Run Once** option have an expiry count.  The expiry count limits the number of times the scheduled request will run.  Independent of how many days or months are selected in the schedule, a scheduled request stops once this number has been reached. Use `-1` if you don't want to limit the number of times that the scheduled request is run.

## Reactivate an expired scheduled request
After a scheduled request has been completed and there are no more recurrences to create a new request, the status is changed to *Expired*.  

**To reuse an expired scheduled request:**
1. In the list of scheduled requests, click **Update** (the pencil icon) on the expired scheduled request that you want to reactivated.
1. Click the clock icon to go to the Scheduling tab.
1. (Optional) Update the schedule.
1. Click **Reactivate**.

## Schedule calendar
You can view all scheduled requests in a calendar view. For each scheduled request, the initial logged request along with its next scheduled event will be displayed in the calendar.

**To access the calendar:**
1. In the list of scheduled requests, click **Schedule Calendar** (the calendar icon).