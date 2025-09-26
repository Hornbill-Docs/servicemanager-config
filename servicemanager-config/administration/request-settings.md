---
layout: article-toc
---
# Request Settings
Use Request Settings to control the behavior of various features on Requests in Service Manager.  These are global settings and any changes will apply to all request types.

## Accessing Request Settings
The Request Settings can be found in the Service Manager Configuration.
* Open configuration (Ctrl+Shift+f).
* In the search box type **Request Settings**.
* In the section titled Service Manager, select **Request Settings**.

## On Hold Settings
Choose which request actions will be enabled when a request is placed on hold. By default, the following actions are enabled:

* Update
* Boards
* Cancel (Only available to those that have the right to cancel requests)

Tick any actions that you wish to allow while requests are on hold, or remove the checkmark from those that you wish to disable. Click **Save** to apply the changes.

Revert any changes to the default settings by clicking **Reset**.

## Resolve Settings
Manage the Resolve settings to control the behavior when resolving requests.

* All manual Resolve/Close without an owner.
* Automatically mark SLM Resolution Timer as part of the resolve action. If using BPM to mark the resolution timer at times other than when resolving, this should be turned off.
* Enable the option to action on linked requests against a request through the Resolve tab.
* Prevent a request from being resolved if it has open activities.
* Enable read-only view of the timeline in the Employee Portal on resolved requests.  This prevents the customer of the request from adding comments to entries in the timeline.
* Enable read-only view of the timeline in the Customer Portal on resolved requests.   This prevents the customer of the request from adding comments to entries in the timeline.

## Customer Section

Choose which customer attributes will be displayed in the Customer Details section on request forms.

* Tick any attributes that you wish to display, or remove the checkmark from those that you wish to hide.
* Revert any changes to the default settings by clicking **Reset to default**.

A customer of a request can be either a user or a contact. As such, you can configure the attributes you wish to display depending on the type of customer of the request.

<!-- service-manager-config/administration/service-manager-assessments>
