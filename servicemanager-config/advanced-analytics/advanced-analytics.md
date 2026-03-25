# Advanced analytics

The advanced analytics module helps you analyze and visualize data within the Hornbill platform. Use this module to create custom reports, dashboards, and data visualizations to understand your service management processes.

## Before you begin

To get started with advanced analytics, ensure you meet the following requirements:

* **User Role**: You must have the **Advanced Analytics User** role. This role allows you to create and view reports, dashboards, and data visualizations.
* **Knowledge**: Review the following concepts to understand the components of advanced analytics and how they work together:
  * [Measures](/esp-config/advanced-analytics/measures)
  * [Widgets](/esp-config/advanced-analytics/widgets)
  * [Dashboards](/esp-config/advanced-analytics/dashboards)
  * [Slideshows](/esp-config/advanced-analytics/slideshows)
* **Database**: Familiarity with the [Service Manager database schema](/servicemanager-external-db/welcome) is helpful for building advanced queries.

## Example: Daily Active Incidents

This example demonstrates how to create a measure to track the number of active incidents on a daily basis, and then visualize this data using a line chart widget on a dashboard.

### Measure

![An example of a measure](/_books/servicemanager-config/images/analytics-measure-example.png)

The goal of this measure is to highlight the number of active incidents in the system on a daily basis. This can help identify trends in incident activity and provide insights into workload and resource allocation.

#### Daily active incidents measure configuration

* **Frequency**: Daily. A new data point will be added to the measure every day at midnight.
* **Value aggregate**: Count. This will count the number of records that match the specified query clause.
* **Maximum sample history**: 12. This means that the measure will retain data for the last 12 days, allowing you to analyze trends over this period.
* **Score card limit**: 10. This limits the number of data points displayed in scorecards to 10.
* **Sparkline limit**: 10. This limits the number of data points displayed in sparklines to 10.
* **Thresholds**: 120, >120 <160, 160. These thresholds can be used to visualize performance against targets, with different colors indicating whether the number of active incidents is within acceptable limits, approaching a warning level, or exceeding the breach threshold.
* **Table**: h_itsm_requests. This is the database table that contains the incident records.
* **Key column**: Request ID(h_pk_reference). This is the unique identifier for each incident record.
* **Query clause**: `h_requesttype = 'incident' AND (h_status = 'status.open' OR h_status = 'status.onHold')`. This clause filters the records to include only those that are classified as incidents and have a status of either open or on hold.

### Widget

With the measure configured, you can now create a widget to visualize the data. In this example, we will create a line chart widget to display the daily active incidents over time.

![An example of a line chart widget](/_books/servicemanager-config/images/analytics-widget-example.png)

#### Daily active incidents line chart widget configuration

* **Widget type**: Data chart. This can be selected under the widget properties. Data charts can include line, bar, and pie charts.
* **Data series**: This is where you select the measure you created for daily active incidents. The widget will use the data from this measure to populate the chart.
* **Chart type**: Line. This will display the data points connected by lines, making it easier to see trends.
* **Sample period**: Start of last month. This will display data from the beginning of the previous month to the current date, allowing you to analyze recent trends in active incidents.  Compared to the measure, which retains data for the last 12 days, this widget will show a broader range of data, providing a more comprehensive view of incident activity over time.

### Dashboard

Finally, you can add the line chart widget to a dashboard to create a visual representation of the daily active incidents. This allows you to monitor this key metric at a glance and share insights with your team.

