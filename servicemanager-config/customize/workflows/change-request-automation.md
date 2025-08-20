---
layout: article-toc
---
# Change Request Automation
## Change Requests
Use these nodes at any stage in a workflow to automate Change Request specific actions.
### Get Information
* **Get Information**<br>Use this Hornbill Automation to get extended change information from a Change Request.

### Suspend
* **Wait for Change Type**<br>Use this Hornbill Automation to suspend the Business Process until a Change Type has been set on the Change Request
* **Wait for Request Schedule**<br>Use this node to pause the process and await the scheduling of the Change Request in the Change Calendar

### Update Request
Apply updates that are specific to Change Requests.

![Update Change Request](/_books/servicemanager-config/images/workflow-update-change.png)

* **Add to Change Calendar**. Use this node to automatically add a change request to the Change Calendar. Use the configuration settings to set the start and end times for the change based on the time this node is invoked in the process. As an example if this node is the first action in a process, then it will use the log time as the Now time, and the Start and End times you configure will be based off that time.
    :::tip
    Use the **Allow Rescheduling** option to overwrite an existing schedule.  When not used, the original schedule will remain in place.
    :::
* **Remove from Change Calendar**. Use this node to automatically remove the Change from the Change Calendar.
* **Change Type**. Use this automation to update the Change Type field on the Change Request.
<!-- https://wiki.hornbill.com/index.php?title=Service_Manager_Business_Process_Workflow -->