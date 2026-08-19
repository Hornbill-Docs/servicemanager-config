---
layout: article-toc
---
# Known Error Automation

Use these nodes at any stage in a workflow to automate Known Error specific actions.

## Get Information

* **Known Error Details**: Use this node to get the Accepted Solution, the Root Cause, and the Workaround from a known error record.

---

## Suspend

The suspend node type is used to suspend a known error record's workflow until the selected task has been completed. This can ensure that the workflow does not continue until the known error record has been updated with the required information.

![Suspend workflow image](/_books/servicemanager-config/customize/workflows/images/suspend-known-error-record-workflow.png)

### Suspend tasks

* **Wait for publishing**: Use this task to suspend the workflow and wait for the known error record to be [published](/servicemanager-user-guide/service-portfolio/requests/publish-action).

### Suspend options

* **Request Id**: The request ID of the known error record to suspend. This is a mandatory field. It is recommended that this be set to **Auto** which will automatically use the request ID of the known error record that is being processed in the workflow. If you select **Manual**, you will need to provide a valid request ID.
* **Expire Period**: When the expire period is reached, the workflow will automatically continue, without the suspend task being completed. The expiry period takes the [Working Time Calendar](/esp-config/customize/working-time-calendars) into consideration when calculating the time that the workflow will resume.
* **Notices**: When a workflow is suspended, it is recommended to display a notice on the known error record to inform users that the workflow is waiting for a task to be completed. You can configure the following options:
  * **Add notice**: Select **Yes** to display a notice on the known error record.
  * **Notice type**: Select either **Alert** or **Information**. An alert will be displayed in a red box, while an information notice will use a blue box.
  * **Notice text**: The notice text that will be displayed.
  * **Notice visibility**: Choose between Service Desk, Portals, or both.

  > **Tip:** Once the suspend task has been completed and the workflow resumes, the notice will be automatically removed.

---

## Update Known Error

* **Update Known Error Details**: Use this node to update the Workaround and Root Cause on a Known Error record.
