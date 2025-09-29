---
layout: article-toc
---
# Service Desk
The Service Desk provides configuration options for defining your Service Desk. Use this to control if a team member or an entire team can be assigned a request.

## Before You Begin
* Log in with a user that has the [Service Desk Admin](/servicemanager-config/setup/service-manager-roles#administration-roles) role.
* Have a general understanding of using [Configuration](/esp-config/getting-started/using-configuration).

## How To Access
1. Search [Configuration](/esp-config/getting-started/using-configuration) for Service Desk.
1. In the results list, select `Service Desk` in the Service Manager section under Administration.

or

1. Open Configuration and select `Service Manager` from the navigation dropdown.
1. In the navigation panel, locate the section titled ***Administration***
1. Select `Service Desk`.

## Teams
The list of teams provided includes all teams that have been defined in the [organization structure](/esp-config/organizational-data/organization).  Each team can be selected to show the members of the team and the current assignment settings.

## Enable Assignment

### Enable or Disable A Member
When viewing a team, each member has an option to enable assignments. When Enable Assignments is `ON`, the user will be available for requests to be assigned to them.

* They can be assigned a request in Intelligent Capture.
* They can be assigned a request from the Assign Action on a request form.
* They can be assigned a request from a workflow that uses either the [Round Robin](/servicemanager-config/customize/workflows/requests-automation#assignment) or [Most Available](/servicemanager-config/customize/workflows/requests-automation#assignment) automation.
* They will receive team assignment notifications.

A Manager who wishes to view the team's requests from the Request List but not be available for assignment can have the Enable Assignment set to `No`.

### Disable An Entire Team
An entire team can have assignment turned off by having the enable assignment set to `No` for all members of that team.  When all members are set to `No`, then:
* The team will not be available for selection in Intelligent Capture.
* The team will not be available for selection from the Assign Action on a request form.
* The team cannot be used with [Round Robin](/servicemanager-config/customize/workflows/requests-automation#assignment) or [Most Available](/servicemanager-config/customize/workflows/requests-automation#assignment) workflow automations.
