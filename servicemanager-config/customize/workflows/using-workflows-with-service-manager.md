---
layout: article-toc
---
# Using Workflows with Service Manager
Workflows are used to drive both manual interactions and automation on a request record.  

## Before You Begin
* Be familiar with how to use the Workflow Designer
* Know how to use Configuration to change application settings

## Where Workflows are Used
Workflows can be used on incidents, requests, problems, known errors, changes, and releases. 

There is a hierarchy of where workflows can be set to determine which workflow is used when a request is raised.

* **Request Catalog Item**<br>This is a request template that is made available on the portals and to the service desk.  A workflow can be associated to each request catalog item.  If no workflow is specified, a default workflow set on the associated service will be used.
* **Service**<br>A default workflow can be specified on a service that will apply to all requests that are are created without using a request catalog item or a workflow has not been specified on the request catalog item.
* **Default Settings**<br>There is a setting for each request type where you can specify which workflow is used. By default these are not set. If a request has not been allocated a workflow by the request catalog item or the service, it will look at these default settings.  If a workflow is not specified in these settings, the request will be raised without a workflow.

    |Setting|Description|
    |-|-|   
    |app.requests.defaultBPMProcess.change|The default workflow to be used when logging a Change and no process is specified.|
    |app.requests.defaultBPMProcess.incident|The default workflow to be used when logging an Incident and no process is specified|
    |app.requests.defaultBPMProcess.knownerror|The default workflow to be used when logging a known error and no process is specified.|
    |app.requests.defaultBPMProcess.problem|The default workflow to be used when logging a Problem and no process is specified.|
    |app.requests.defaultBPMProcess.release|The default workflow to be used when logging a Release and no process is specified.|
    |app.requests.defaultBPMProcess.service|The default workflow to be used when logging a Service Request and no process is specified.|

## Workflow Tracker
The Workflow Tracker is a graphical representation of the workflow that is displayed at the top of a request. This is an optional display which uses stages and checkpoints within a workflow to visualize the progress. The workflow tracker will be displayed when:
* On a single stage workflow, at least one checkpoint has been set up.
* There is more than one stage in a workflow.

## How Workflows Work
### Workflow Definitions
The workflow definitions are those that you create and define within the [workflow designer](/servicemanager-config/customize/workflows/workflow-designer). Each workflow definition includes:
* Workflow nodes and logic.
* Language definitions.
* All previous versions for that workflow.
* Workflow settings

### Workflow Instances
When a request is created, an *instance* or copy of the associated workflow definition is also created. This workflow instance is taken from the active version of the published workflow. These workflow instances can be viewed and managed under the `Manage Executed Workflows`.  If a workflow definition is updated and a new version is published, the workflow instances are not updated. Once a workflow instance is created, it will continue to use the workflow version under which it was created.

:::info
Each workflow instance is still dependant on the workflow definition from which it was created.  A workflow instance will reference the workflow definition for language translations and other settings.  Because of this dependency, a workflow definition cannot be deleted while there are active instances of that workflow.
:::

## Using Workflow Utilities
Hornbill provides [a set of workflow utilities](https://www.hornbill.com/hubfs/LMS/Course-Resources/Live%20-%20Workflow%20automation/Hornbill%20Workflow%20Utilities.pdf) that can be used to facilitate date-related functions as well as operations to convert and manipulate data.

cleanse data
concatenate strings
get dates and timestamps
format dates

For example, you can ____
to convert characters in a string from uppercase to lowercase


## Further Learning
Explore courses in Hornbill Academy:
* [Workflow automations overview](https://academy.hornbill.com/app/courses/6ef4aeb5-26ba-45c5-bc89-78181d2ab62b)