# Employees Widget

The Employees widget is part of the [People Hub for NHS Trusts](https://www.hornbill.com/solutions/nhs-hrsm/) solution and is available to registered users.

The Employees widget shows a list of employees managed by the signed-in user. It can also show user availability, online status, an overall availability summary, and a compact layout for smaller portal areas.

## What the widget shows

The widget displays employee profile information and optional availability information, depending on the configuration selected by the administrator.

![Employees widget example](/_books/servicemanager-config/employee-portal/images/employees-widget.png)

## Which employees are shown

The widget is designed to show employees managed by the signed-in user. It uses the signed-in user as the manager filter. If the signed-in user does not manage any employees, the widget will be empty.

## Administrator configuration

Administrators can control which availability and layout options are used by the widget.

| Configuration option | Purpose | Recommended use |
| --- | --- | --- |
| Show availability and online status | Shows status indicators such as Online, Inactive, Mobile, Offline, and availability labels. | Use when managers need to see whether team members are currently available. |
| Show overall availability | Shows a summary banner, such as how many listed users are currently available. | Use on team dashboards where managers need a quick availability count. |
| Show minimal layout | Displays a more compact version of the user list. | Use when the widget is placed in a narrow column or a portal homepage with limited space. |
| Refresh automatically to get status updates | Refreshes the widget periodically while the page is active. | Use when online or availability status needs to stay up to date without manual refresh. |

> ℹ️ **Recommendation:** Enable availability and online status together with automatic refresh when the widget is being used as a live team availability view. Use minimal layout when the widget sits beside other portal content.

## Availability information

The widget can show two types of availability information: individual status per employee and an overall availability summary.

### Individual user status

When enabled, each user can show their current online or availability status. Examples include Online, Inactive, Mobile, and Offline.

### Overall availability

When enabled, the widget shows a summary of how many listed users are currently available. If all listed users are available, it can show a message such as all users are available. Otherwise, it shows the available count compared with the total number of listed users.

| Summary type | Example |
| --- | --- |
| All available | All 5 are available |
| Some available | 3 available users out of 5 |

## Layout options

The widget supports a standard layout and a minimal layout.

### Standard layout

Shows a larger user image or avatar, the employee name, and any configured status text.

### Minimal layout

Shows a compact row with a small status icon and the employee name. This uses less vertical space.

![Employees widget minimal layout example](/_books/servicemanager-config/employee-portal/images/employees-widget-minimal.png)

## Localization and customization strings

The following strings are used by the Employees widget and its configuration.

| Key | Default value | Where it is used |
| --- | --- | --- |
| `employeePortal.widgets.employees.config.name` | Employees | Widget name shown in the page builder. |
| `employeePortal.widgets.employees.config.description` | Employees that are managed by me. | Widget description shown in the page builder. |
| `user.view.catalog-widgets.users.show-availability-and-online-status` | Show availability and online status | Configuration checkbox label. |
| `user.view.catalog-widgets.users.show-overall-availability` | Show overall availability | Configuration checkbox label. |
| `user.view.catalog-widgets.users.show-minimal-layout` | Show minimal layout | Configuration checkbox label. |
| `user.view.catalog-widgets.users.auto-refresh-desc` | Refresh automatically to get status updates | Configuration checkbox label. |
| `user.sm.online` | Online | User online status. |
| `user.sm.inactive` | Inactive | User inactive status. |
| `user.sm.mobile` | Mobile | User mobile status. |
| `user.sm.offline` | Offline | User offline status. |
| `user.sm.page.widget.users.available-users-all` | All %1 are available | Overall availability summary when all listed users are available. |
| `user.sm.page.widget.users.available-users-not-all` | %1 available users out of %2 | Overall availability summary when only some listed users are available. |

## FAQs

| Question | Answer |
| --- | --- |
| Who is shown in the widget? | The widget shows active employees managed by the signed-in user. |
| Can the manager be changed from the widget? | No. The widget uses the signed-in user as the manager. |
| Why is the widget empty? | The signed-in user may not manage any active employees, or there may be no matching employee records. |
| What does automatic refresh do? | It periodically reloads the widget while the page is active so availability and online status can stay current. |
| When should minimal layout be used? | Use it when the widget is placed in a narrow column, on a homepage, or next to other content where space is limited. |
