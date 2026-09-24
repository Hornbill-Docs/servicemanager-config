# Employee Assignments Widget

The Employee Assignments widget is part of the [People Hub for NHS Trusts](https://www.hornbill.com/solutions/nhs-hrsm/) solution and is available to registered users

The Employee Assignments widget gives managers a view of employee assignment records for people they supervise. It is intended for Employee Portal pages where a manager needs quick access to assignment details such as position, department, FTE, assignment category, status, and assignment end date.

![Employee Assignments widget screenshot](/_books/servicemanager-config/employee-portal/images/employee-assignments-widget.png)

## What the widget shows

The widget retrieves assignment records that match the signed-in user as supervisor. The widget also applies a default list of assignment statuses when no specific status is selected.

| Area | Behavior |
| --- | --- |
| Supervisor scope | Results are filtered using the signed-in user as the supervisor. |
| Employee scope | The table shows assignment records for employees managed by that supervisor. |
| Default statuses | Includes active and common in-progress assignment statuses such as Active Assignment, Acting Up, Internal Secondment, Career Break, Maternity and Adoption, External Secondment, and Suspend With Pay. |
| Bank posts | Bank posts are included unless the operation is explicitly called with bank posts excluded. |
| Past assignments | Past assignments are included unless the operation is explicitly called with past assignments excluded. |
| Module dependency | The widget only loads assignment data when the Employee Management module setting is enabled. |

## User experience

* **Search**: Users can search by employee name or assignment number. Search input is trimmed before the request is sent.
* **Status filtering**: Users can filter the list by assignment status from the status dropdown.
* **Employee profile display**: The employee column includes the employee profile image and name where available.
* **Pagination**: Results are paged to keep the table readable. The default page size is 10 records.

## Search and status filters

### Search

The search box filters assignments using a partial match. The backend search checks the employee name and assignment number.

| User action | Result |
| --- | --- |
| Type an employee name | Returns assignments where the employee name contains the search text. |
| Type an assignment number | Returns assignments where the assignment number contains the search text. |
| Clear the search box | Returns the list using the selected status filter only. |

### Status filter options

| Status option | Recommended use |
| --- | --- |
| Acting Up | Use when managers need to see temporary acting-up assignments. |
| Active Assignment | Use for current active assignments. |
| Internal Secondment | Use for internal secondment records. |
| Career Break | Use for employees currently recorded against a career break assignment status. |
| Maternity and Adoption | Use for assignment records related to maternity or adoption leave. |
| Out on External Secondment Paid | Use for paid external secondment assignments. |
| Out on External Secondment Unpaid | Use for unpaid external secondment assignments. |
| Suspend With Pay | Use for employees recorded with a suspended with pay assignment status. |

## Assignment table fields

The widget displays a fixed assignment table. The visible columns are designed to provide manager-friendly assignment context without requiring users to open the full assignment record.

| Column | Field shown | Recommended use |
| --- | --- | --- |
| ASG No | Assignment number | Useful for identifying the assignment record. |
| Employee Name | Employee profile image and name | Useful for quickly identifying the employee. |
| Department | Department | Useful for organizational context. |
| Position No | Position number | Useful for HR and workforce planning references. |
| Position Title | Position title | Useful for understanding the employee role. |
| Actual FTE | Actual FTE value | Useful for understanding working-time allocation. |
| ASG Category | Assignment category | Useful for distinguishing assignment types such as permanent, temporary, or bank-related records. |
| ASG Status | Assignment status | Useful for lifecycle and operational status context. |
| ASG End Date | Assignment end date | Useful for identifying assignments that are due to end. |

> ℹ️ **Recommendation:** Use this widget on pages intended for managers or supervisors. The table contains several HR-style fields, so it is best suited to pages where users expect detailed assignment information.

## Administrator configuration

The current configuration panel for this widget does not expose customer-editable options. The widget follows its built-in behavior and uses the signed-in user as the supervisor filter.

| Configuration area | Current behavior |
| --- | --- |
| Visible configuration options | No visible options are currently shown in the configuration panel. |
| Records per page | Defaults to 10 records per page. |
| Supervisor filter | Uses the signed-in user automatically. |
| Employee Management module | The widget requires the Employee Management module setting to be enabled before data is loaded. |

## Responsive layout

The widget displays assignment data in a table. Tables work well for detailed HR-style data, but they need enough horizontal space to remain readable.

* On wide screens, the table can show all assignment fields in one row.
* On medium screens, the table may need horizontal scrolling depending on the portal layout and widget width.
* On small screens, users may need to scroll horizontally to view all columns. This avoids squeezing important field values into unreadable text.

> ⚠️ **Layout note:** Because this widget contains many columns, it is usually better on wider portal sections or pages where detailed assignment information is expected.

## Localization and customization strings

The widget currently uses a mixture of translated strings and fixed labels. The following visible labels are used by the widget.

| Area | Key or label | Default value |
| --- | --- | --- |
| Status | `Acting Up` | Acting Up |
| Status | `Active Assignment` | Active Assignment |
| Status | `Internal Secondment` | Internal Secondment |
| Status | `Career Break` | Career Break |
| Status | `Maternity and Adoption` | Maternity and Adoption |
| Status | `Out on External Secondment Paid` | Out on External Secondment Paid |
| Status | `Out on External Secondment Unpaid` | Out on External Secondment Unpaid |
| Status | `Suspend With Pay` | Suspend With Pay |
| User presence | `user.sm.online` | Online |
| User presence | `user.sm.inactive` | Inactive |
| User presence | `user.sm.mobile` | Mobile |
| User presence | `user.sm.offline` | Offline |
| Search placeholder | Fixed label | Search... |
| Status placeholder | Fixed label | filter by status |
| Empty state | `ui.app.com.hornbill.servicemanager.operation.link.noResults` | No results found |
| Table header | Fixed label | ASG No |
| Table header | Fixed label | Employee Name |
| Table header | Fixed label | Department |
| Table header | Fixed label | Position No |
| Table header | Fixed label | Position Title |
| Table header | Fixed label | Actual FTE |
| Table header | Fixed label | ASG Category |
| Table header | Fixed label | ASG Status |
| Table header | Fixed label | ASG End Date |

> ℹ️ **Recommendation:** If this widget is intended for wider customer use, consider moving fixed labels into translation keys so administrators can localize all visible text consistently.

## Frequently asked questions

| Question | Answer |
| --- | --- |
| Why do I only see certain employees? | The widget filters assignments by the signed-in user as supervisor. |
| Why are there no results? | There may be no matching supervised assignments, the selected status may not match any records, or the Employee Management module may not be enabled. |
| Can administrators configure which columns are shown? | No visible column configuration is currently exposed in the widget configuration panel. |
| Can users search by any field? | The current backend search checks employee name and assignment number. |
| Why is the table wide? | The widget shows detailed assignment information. A table layout preserves the field structure and keeps values readable. |
