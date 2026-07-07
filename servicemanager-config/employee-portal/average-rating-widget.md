# Average Rating Widget

The Average Rating widget displays the average star rating from [feedback](/servicemanager-user-guide/service-portfolio/customer-feedback) on closed requests. It is useful for Employee Portal dashboards where customers want to see how service feedback is trending across the instance or within a specific service domain.

| Purpose | Optional domain filter | Optional time period |
| --- | --- | --- |
| Show the average rating submitted against requests. | Administrators can filter the widget by Service Domain so the result is focused on a specific area of services. | Administrators can show the average for all time or only for ratings received during a recent period. |

## What the widget shows

The widget displays a circular rating visual, the average rating value, the selected time period, and the number of ratings included in the result.

![Average Rating](/_books/servicemanager-config/images/ep-rating-widget.png)

| Displayed item | Meaning |
| --- | --- |
| Average rating | The rounded average of request star ratings included in the query. |
| Rating circle | A visual ring that changes progress and color based on the average rating value. |
| Time period label | Shows whether the average is for all time or for a configured number of days. |
| Ratings count | The number of request ratings included in the average. |
| No ratings message | Displayed when there are no ratings for the configured domain and time period. |

### Rating color thresholds

The rating circle color changes based on the average rating between 1 and 5.

|Threshold|Color|
|---|---|
|2.0 or below|Shown in red.|
|Above 2.0 to 3.5|Shown in orange.|
|Above 3.5|Shown in green.|

---

## Administrator configuration

Administrators can configure whether the widget is filtered by Service Domain and which time period should be used.

| Configuration option | Purpose | Recommended use |
| --- | --- | --- |
| Filter by Service Domain | Enables the Service Domain selector. | Use this when the portal page is focused on a particular domain or when feedback should be reported separately by service area. |
| Service Domain | Selects the domain used to filter request ratings. | Choose the domain that matches the portal page or the service reporting area. |
| Last X Days | Limits the average to ratings from recently closed requests. | Use a time period when the widget should show recent feedback trends rather than lifetime average. |

### Available time period options

| Option | Displayed meaning |
| --- | --- |
| Blank | The widget displays the generic Average label and does not apply a date period. |
| 30 | Average over the last 30 days. |
| 60 | Average over the last 60 days. |
| 90 | Average over the last 90 days. |
| 180 | Average over the last 180 days. |

> **Recommendation:** Use 30 or 90 days for a current feedback view. Use a blank period if the widget is intended to show the overall average across all available ratings.

---

## How the rating is calculated

The widget calculates an average from request feedback star ratings that match the selected configuration.

| Rule | Customer-facing explanation |
| --- | --- |
| Average rating | The displayed value is the average of the star ratings included in the selected scope. |
| Rating count | The count shows how many ratings were used to calculate the average. |
| Service Domain filter | When a Service Domain is selected, only ratings from requests linked to services in that domain are included. |
| No domain selected | The widget shows the average across rated requests for services that belong to a Service Domain. |
| Days filter | When a time period is selected, only ratings from requests completed during that period are included. |
| Unrated requests | Requests without a star rating are not included in the average. |

---

## User experience

| Quick visual feedback | Rating volume shown |
| --- | --- |
| The rating value, star icon, and colored circle make the result easy to scan. | The widget shows the number of ratings so users can understand how much feedback supports the average. |

| Recent or overall view | Clear empty state |
| --- | --- |
| The time period label makes it clear whether the value is recent or general. | If there are no ratings for the selected scope, the widget tells users that no star ratings have been received yet. |

---

## Responsive layout

The widget is designed as a compact visual card and works well in portal homepage areas or service-focused pages.

| Page layout | Expected behavior |
| --- | --- |
| Wide portal area | The circle and text are centered and remain visually prominent. |
| Narrow portal column | The widget remains compact, with the rating as the main focus. |
| Mobile or small screens | The widget content stacks naturally and avoids horizontal scrolling. |

---

## Localization and customization strings

The following strings are used by the Star Feedback widget and its configuration.

| Key | Default value | Where it is used |
| --- | --- | --- |
| `employeePortal.employeePortal.widgets.average` | Average | Generic label when no number of days is shown. |
| `employeePortal.employeePortal.widgets.average1Day` | Average over the last day | Used if the configured period is 1 day. |
| `employeePortal.employeePortal.widgets.averageXDays` | Average over the last $days days | Used when the configured period is more than 1 day. The token `$days` is replaced by the selected value. |
| `employeePortal.employeePortal.widgets.ratingsCount` | $count Ratings | Shows the number of ratings included in the average. The token `$count` is replaced by the rating count. |
| `employeePortal.widgets.notEnough.ratings` | We haven't received any star ratings yet | Shown when no ratings are available for the selected scope. |

---

## Frequently asked questions

| Question | Answer |
| --- | --- |
| What does the rating represent? | It represents the average star rating from request feedback included in the widget's configured scope. |
| Why does the widget show no ratings? | There may be no request ratings in the selected Service Domain or time period. |
| Can the widget be limited to one Service Domain? | Yes. Enable Filter by Service Domain and select the domain in the widget configuration. |
| Does the widget include unrated requests? | No. Only requests with a rating greater than zero are included. |
| Which time period should be used? | Use 30 or 90 days for current feedback trends. Use the blank option for an overall average. |
