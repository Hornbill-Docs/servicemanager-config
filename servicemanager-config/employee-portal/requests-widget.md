# Requests Widget

The Requests widget lets Employee Portal users view and manage requests that are relevant to them from the Employee Portal page. It supports My Requests, Connections, and My Staff's Requests where enabled.

- **Default view:** My Requests
- **Main filters:** Active, Closed, Awaiting Feedback
- **Search:** Reference or summary
- **Audience:** Employee Portal users

![Request Widget](/_books/servicemanager-config/images/ep-requests-widget.png)

---

## What requests are shown

The request list depends on the selected request view and status filter.

| View | Shown in the widget | When to use |
| --- | --- | --- |
| My Requests | Requests raised by the signed-in user. | Best for normal self-service pages where users mainly track their own tickets. |
| Connections | Requests where the signed-in user is added as a connection and the connection is allowed to display the request. | Best when users need to follow requests they did not raise themselves. |
| My Staff's Requests | Requests for users managed by the signed-in person. | Best for managers. This view is shown only when staff requests are enabled and the user manages at least one person. |
| Awaiting Feedback | Requests awaiting feedback from the user. | Best for quickly prompting users to complete feedback where feedback requests exist. |

### Status filters

| Status option | Meaning |
| --- | --- |
| Active | Shows requests in active portal states, including Open, New, On Hold, and Resolved. |
| Closed | Shows closed requests. |
| Awaiting Feedback | Shows requests where feedback is pending. This option is shown only when there are requests awaiting feedback. |

> **Request types:** Incident and Service Request are included by default. Change Requests can also be included when the relevant Service Manager setting is enabled.

---

## User experience

**Search**
Users can filter the list using the search box. The search is intended for partial matches against request reference or summary.

**Status filter**
Users can switch between Active and Closed requests. Awaiting Feedback appears when feedback is waiting for the user.

**Request view filter**
Users can switch between My Requests, Connections, and My Staff's Requests where those views are available.

**Pagination**
The widget paginates results when there are more requests than can fit on one page.

**Export**
If export is enabled, users can download request results from the widget. Export is available on desktop and generic layouts.

**No requests**
If no matching requests are found, the widget shows a simple no requests message.

---

## Administrator configuration

The widget configuration controls the starting view and whether the widget follows the service domain context of the page.

| Configuration option | What it does | Recommended use |
| --- | --- | --- |
| Disable filtering by Service Domain | Stops the widget from automatically filtering by the service domain where the widget is placed. | Use this when the widget should show relevant requests across the portal instead of only the current domain. |
| Default Request View: My Requests | Opens the widget using requests raised by the signed-in user. | Recommended for most portal homepages. |
| Default Request View: Connections | Opens the widget using requests where the user is connected. | Useful for collaboration-focused portals. |
| Default Request View: My Staff's Requests | Opens the widget using requests raised by staff managed by the signed-in user. | Useful on manager pages. This option is available only when staff requests are enabled. |

> **Configuration note:** If My Staff's Requests is selected as the default view but staff requests are not enabled, the widget falls back to My Requests.

---

## Recommended use

| Scenario | Recommended configuration | Reason |
| --- | --- | --- |
| General Employee Portal homepage | Default Request View: My Requests | Most users expect to see the tickets they raised first. |
| Service-specific page | Keep domain or service filtering enabled | Users see requests relevant to that service area. |
| Company-wide request overview | Disable filtering by Service Domain | Users can see relevant requests across domains. |
| Manager portal page | Default Request View: My Staff's Requests | Managers can quickly see requests raised by their staff. |
| Collaboration-heavy process | Default Request View: Connections | Users can track requests where they are involved, even if they did not raise them. |

> **Recommendation:** Use My Requests for general portal homepages. Use Connections or My Staff's Requests only where the page is designed for collaboration or manager activity.

---

## Responsive layout

The widget adjusts the number of records shown per page depending on the widget placement and screen size.

- On standard layouts, the widget commonly shows three requests per page.
- When the widget is placed in a wider area with more columns, it can show more requests per page.
- On mobile layouts, controls and list spacing are reduced so the widget remains readable.
- Pagination is shown when the total number of matching requests is greater than the number of records shown per page.

> **Best practice:** Keep the widget compact on portal homepages. Use a wider layout when users are expected to work with longer request lists.

---

## System settings that affect behavior

The widget can change behavior based on Service Manager settings.

| Setting | Behavior affected |
| --- | --- |
| `guest.servicemanager.portal.additionalRequestTypes.change` | Allows Change Requests to be included with Incident and Service Request records. |
| `servicemanager.portal.requests.showStaffRequests` | Controls whether My Staff's Requests can be shown. |
| `guest.servicemanager.portal.requestList.export` | Controls whether users can export request list results. |
| `api.xmlmc.queryExec.maxResultsAllowed` | Controls the maximum number of rows that can be exported. |

---

## Localization and customization strings

The following keys can be used to customize the widget text.

| Key | Default value |
|---|---|
| `guest.com.hornbill.servicemanager.portals.servicePortal.home.requestView.reference` | Reference |
| `guest.com.hornbill.servicemanager.portals.servicePortal.home.requestView.summary` | Summary |
| `guest.com.hornbill.servicemanager.portals.servicePortal.home.requestView.service` | Service |
| `guest.com.hornbill.servicemanager.portals.servicePortal.home.requestView.catalog` | Catalog Item |
| `guest.com.hornbill.servicemanager.portals.servicePortal.home.requestView.details.customer` | Customer |
| `guest.com.hornbill.servicemanager.portals.servicePortal.home.requestView.datelogged` | Date Logged |
| `guest.com.hornbill.servicemanager.portals.servicePortal.home.requestView.status` | Status |
| `guest.com.hornbill.servicemanager.portals.servicePortal.home.requestView.subStatus` | Sub-status |
| `guest.com.hornbill.servicemanager.portals.servicePortal.home.requestView.filter` | Filter |
| `guest.com.hornbill.servicemanager.portals.servicePortal.home.requestView.active` | Active |
| `guest.com.hornbill.servicemanager.portals.servicePortal.home.requestView.closed` | Closed |
| `guest.com.hornbill.servicemanager.portals.servicePortal.home.requestView.awaitingFeedback` | Awaiting Feedback |
| `guest.com.hornbill.servicemanager.portals.servicePortal.requestlist.filter.defaultView` | Default Request View |
| `guest.com.hornbill.servicemanager.portals.servicePortal.requestlist.filter.myRequests` | My Requests |
| `guest.com.hornbill.servicemanager.portals.servicePortal.requestlist.filter.myStaffRequests` | My Staff's Requests |
| `guest.com.hornbill.servicemanager.portals.servicePortal.requestlist.filter.connections` | Connections |
| `guest.com.hornbill.servicemanager.portals.employeePortal.getResults` | Download Results |
| `guest.com.hornbill.servicemanager.portals.servicePortal.home.requestView.noRequests` | There are no requests |
| `guest.com.hornbill.servicemanager.portals.employeePortal.status` | Request Status |
| `guest.com.hornbill.servicemanager.portals.servicePortal.home.requestView.noSummary` | No Summary Available |
| `user.view.requests.exportRowLimit` | We have exported the first %1 requests. If you need to export more, please contact your System Administrator who can increase the limit by changing the system setting api.xmlmc.queryExec.maxResultsAllowed |
| `user.view.catalog-widgets.services.TODO` | Disable filtering by Service Domain |

---

## Frequently asked questions

| Question | Answer |
| --- | --- |
| Why do I not see My Staff's Requests? | The option appears only when staff requests are enabled and the signed-in user manages at least one person. |
| Why do I not see Awaiting Feedback? | The option is shown only when the user has requests awaiting feedback. |
| Why does the list show only requests from one area? | The widget may be using the current service domain or service context. Administrators can disable service domain filtering if the widget should show requests across domains. |
| Why do I not see Change Requests? | Change Requests are included only when the relevant Service Manager setting is enabled. |
| Why is export not visible? | Export depends on the export setting and the current layout. It is available for desktop and generic layouts when enabled. |
| What happens when there are no matching requests? | The widget shows the configured no requests message. |
