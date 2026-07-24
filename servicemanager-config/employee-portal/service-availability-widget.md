# Service Availability Widget

The Service Availability widget gives Employee Portal users a simple percentage view of how available a selected service has been over a chosen time period.

- **Widget name:** Service Availability
- **Audience:** Employee Portal users
- **Display:** Availability percentage
- **Configuration:** Service and time period

## Overview

**Customer facing** — The Service Availability widget is designed to show a quick availability summary for a service. It is useful on Employee Portal pages where users need a simple indication of service health over a recent period.

**Purpose**
Show the percentage of time a service has been available during the configured time period.

**Service focused**
The widget can be configured to show availability for a selected service.

**Simple display**
The widget displays a large percentage, an icon, the time period label, and the service name.

> **Customer summary:** Add this widget to portal pages where users need a quick service availability indicator, such as a service homepage or service status area.

## What the widget shows

The widget shows a percentage based on service status history for the configured service and date range.

![Service Availability](/_books/servicemanager-config/images/ep-service-availability-widget.png)

> **Example**: ✅ **100%** Availability over the last 90 days for the service **Desktop Support**

### Availability color thresholds

The percentage is color-coded to make the result easier to understand at a glance.

| Range | Color |
| --- | --- |
| 95% and above | Green |
| 90% to 94% | Orange |
| Below 90% | Red |

| Displayed item | Meaning |
| --- | --- |
| Availability percentage | The calculated percentage of available time for the selected period. |
| Status icon | A visual indicator displayed next to the percentage. |
| Time period label | Shows whether the value is for availability generally, the last day, or the last configured number of days. |
| Service name | Shows the name of the configured service when it is available. |
| Not enough information message | Shown when there is not enough service status history to calculate a percentage. |

## Administrator configuration

Administrators configure the widget by selecting the service and, optionally, the number of days to include in the availability calculation.

| Configuration option | Purpose | Recommended use |
| --- | --- | --- |
| Service ID | Selects the service that the widget should report availability for. | Use a service that users recognize and that has meaningful service status history. |
| Last X Days | Controls the date range used for the availability percentage. | Use a period that matches the purpose of the page. For example, 30 days for recent health or 90 days for a longer operational view. |

### Available time period options

| Option | Displayed meaning |
| --- | --- |
| Blank | The widget displays the generic Availability label. |
| 1 | Availability over the last day. |
| 30 | Availability over the last 30 days. |
| 60 | Availability over the last 60 days. |
| 90 | Availability over the last 90 days. |
| 180 | Availability over the last 180 days. |

> **Recommendation:** Use 30 or 90 days for most Employee Portal pages. Very short periods can change quickly, while very long periods may hide recent service problems.

## How availability is calculated

The widget checks the service status history for the selected time period. It uses the time spent in the available state and compares it with time spent in negative states.

| Status group | How it is used |
| --- | --- |
| Available | Counts as available service time. |
| Impacted | Counts as unavailable or negative service time for the widget calculation. |
| Unavailable | Counts as unavailable or negative service time for the widget calculation. |

The widget calculates the percentage using this approach:

> **Calculation:** Availability percentage = available time divided by available time plus impacted and unavailable time.

If the service status history does not include enough data for the selected period, the widget displays a message instead of a percentage.

## User experience

**Fast summary**
Users can quickly understand whether the configured service has been mostly available in the selected period.

**Simple wording**
The text explains the period, such as availability over the last 30 days.

**Service context**
The service name is displayed below the availability label so users know which service the value belongs to.

**Fallback message**
When there is not enough information for the time period, the widget shows a clear message rather than an empty result.

## Responsive layout

The widget uses a compact layout that works well in small portal spaces. The main percentage is displayed prominently and the supporting text appears below it.

| Page layout | Expected behavior |
| --- | --- |
| Wide portal area | The percentage, label, and service name are centered and easy to scan. |
| Narrow portal column | The widget remains compact, with the percentage as the main focus. |
| Mobile or small screens | The widget content stacks naturally and avoids horizontal scrolling. |

## Localization and customization strings

The following strings are used by the Service Availability widget and can be localized.

| Key | Default value | Where it is used |
| --- | --- | --- |
| `employeePortal.employeePortal.widgets.availability` | Availability | Generic label when no number of days is shown. |
| `employeePortal.employeePortal.widgets.availability1Day` | Availability over the last day | Displayed when the widget is configured for 1 day. |
| `employeePortal.employeePortal.widgets.availabilityXDays` | Availability over the last $days days | Displayed when the widget is configured for more than 1 day. The token `$days` is replaced with the configured value. |
| `employeePortal.widgets.notEnough.data` | Not enough information available for the time period | Displayed when the widget cannot calculate an availability percentage. |
| `user.view.catalog-widgets.my-requests.service-domain` | Service ID | Configuration label for selecting the service. |
| `user.view.catalog-widgets.my-requests.service-domain` | Last X Days | Configuration label for choosing the availability period. |

> **Note:** The configuration labels currently share the same translation key in the supplied configuration markup. If separate localization is required, use separate keys for Service ID and Last X Days.

## Customer notes

| Question | Answer |
| --- | --- |
| What does the percentage mean? | It represents the percentage of available time for the selected service during the configured period. |
| Why does the widget show not enough information? | The selected service may not have enough status history in the configured period to calculate availability. |
| Can the widget show any service? | The service list is based on services available to the logged-on person, and the service status history operation checks service access before returning data. |
| Does the widget show detailed outage history? | No. This widget shows a summary percentage. Detailed history is handled by the service status history data behind the calculation. |
| Which time period should be used? | For most portal pages, 30 or 90 days gives a useful balance between recent service health and enough data for a stable calculation. |
