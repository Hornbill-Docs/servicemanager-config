---
layout: article-toc
---
# Manage Executed Workflows
The executed workflows consist of all the workflow instances that have been created from workflow definitions.  Each workflow instance will be associated to an individual Service Manager request.

The executed workflows are divided by their current status.
* **Running**. The workflow instance is active but it will be waiting for the completion of a human task or authorization before continuing. 
* **Completed**.  The workflow instance has successfully reached the end. There is no further processing.
* **Failed/Canceled**. Failed workflow instances will have reached an error on one of the workflow nodes. Canceled workflow instances will have either been manually canceled, or canceled as a result of the associated request being canceled.
* **Suspended**. A suspended workflow has been temporarily paused by a Hornbill Automation that requires some form of action before it will continue.

## Workflow Instance List
### Actions
* **Workflow Logging Information**.  This is a detailed log of all the events that have occurred.
    :::info
    Logs get deleted after 1 week for a succesfully completed workflow, and after 3 months for a failed or canceled workflows. 
    :::
* **Workflow Info**. Displays the Workflow Tracker, the date of the last update, and details of an error if the workflow has failed.
* **Restart Workflow**. This will restart the workflow from the very start. This should be used carefully as it may result in some automations being repeated.
* **Resume Workflow**. This will resume the workflow from the current node. This can be used when a failed node has been corrected.
* **Cancel Workflow**. Stops the workflow at its current location.  The [Workflow Tracker](/servicemanager-config/customize/workflows/using-workflows-with-service-manager#workflow-tracker) on the request will continue to be displayed and show at what point it was canceled. Canceled workflows cannot be restarted.
* **Delete Workflow**. A deleted workflow will be completely removed from the assocated request.  The Workflow Tracker will no longer be visible on the request.
