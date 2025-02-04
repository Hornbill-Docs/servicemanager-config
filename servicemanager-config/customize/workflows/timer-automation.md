# Timers
The timers are used to track the progress of a request against a [service level target](/servicemanager-user-guide/service-portfolio/service-level-agreements/service-levels#service-level-targets) as defined in the associated [Service Level Agreement (SLA)](/servicemanager-user-guide/service-portfolio/service-level-agreements/overview). Use the timer automations at any point within a workflow to either start or stop the response and resolution timers.

The benefit of using timers within a workflow is to provide control over what conditions need to be met before a timer is started, paused, or marked.  

## Before you begin
Before timers can be utilized, at least one [Service Level Agreement (SLA)](/servicemanager-user-guide/service-portfolio/service-level-agreements/overview) needs to be defined with service levels that include response and resolution targets.
* A request that utilizes a workflow with timers needs to be associated with a [service](/servicemanager-user-guide/service-portfolio/services/overview). Service selection is typically done using the [Services Form](/servicemanager-config/customize/service-manager-capture-forms#services) in [Intelligent Capture](/servicemanager-config/customize/service-manager-capture).
* A request that uses a workflow with a response timer must be associated with a service that has a [Service Level Agreement (SLA)](/servicemanager-user-guide/service-portfolio/service-level-agreements/overview) with a response target set up.  
* A request that uses a workflow with a resolution timer must be associated with a service that has a [Service Level Agreement (SLA)](/servicemanager-user-guide/service-portfolio/service-level-agreements/overview) with a resolution target set up.

## How to add a timer
1. Add a Hornbill Automation node to the workflow.
1. Open the node's settings by clicking on the cog icon.
1. Under the Scope field select `Application`.
1. Under the type field select `Timer`.
1. Under the task field select the required type of timer.

![Timers](/_books/servicemanager-config/customize/workflows/images/timers.png)

## Response timers
Response Time refers to the amount of time it takes from the moment a new request is raised to when it is actively being worked on.  Once a response timer has started, any number of conditions can be included in the workflow that determines when the response time should be marked.  Conditions that might be considered are:
* The completion of an [assessment](/servicemanager-config/administration/assessment-levels).
* The assignment to a team.
* The assignment of an owner.
* An acknowledgment to the customer that the request has been received.

### Response tasks
* **Start Response Timer**. The Start Response Timer works in conjunction with the Mark Response Time. While the timer is running, it is used to track the service level response target based on the service level that has been associated with the request.
* **Mark Response Time**. The Mark Response Time works in conjunction with the Start Response Timer.  When the Mark Response Time is reached in the workflow, the Response Timer is stopped and the date and time are marked in the request.  

## Resolution timers
Resolution time refers to the amount of time it takes to resolve a request. The point at which a resolution timer starts can vary from workflow to workflow.  In some cases, the resolution timer may start at the same time as the response timer.  The response timer could also start after the response time has been marked, at which point the request has been assessed, assigned, and can now be worked on.

### Settings
Some [application settings](/servicemanager-config/advanced-tools-and-settings/application-settings) that control the default behavior of the resolution timers after they have started. The following settings are available to automatically pause, resume, or stop the resolution timer when the status of a request changes.

* app.request.pauseResolutionTimerOnResolve (Default OFF)
* app.request.resumeResolutionTimerOnReopen (Default OFF)
* app.request.stopResolutionTimerOnResolve (Default ON)
* app.request.stopResolutionTimerOnClose (Default OFF)

:::info
The `app.request.stopResolutionTimerOnResolve` setting will take precedence over the `app.request.pauseResolutionTimerOnResolve` setting if they are both turned `ON`.  
:::
:::tip
Before setting up a resolution timer in a workflow, check these settings as they may influence how resolution times are marked over what has been added to the workflow.
:::

### Resolution tasks
* **Start Resolution Timer**. The Start Resolution Timer works in conjunction with the Mark Resolution Time.  While the timer is running, it is used to track the service level resolution target based on the service level that has been associated with the request.
* **Mark Resolution Time**. The Mark Resolution Time works in conjunction with the Start Resolution Timer. When the Mark Resolution Time is reached in the workflow, the Resolution Timer is stopped and the date and time are marked in the request. 
* **Pause Resolution Timer**.  This automation needs to be between a Start Resolution Timer and a Mark Resolution Time.  This will pause the resolution timer until either the Resume Resolution Timer or Mark Resolution Time is reached.
* **Resume Resolution Timer**. This will resume a Resolution Timer that has been paused using the Pause Resolution Timer.
