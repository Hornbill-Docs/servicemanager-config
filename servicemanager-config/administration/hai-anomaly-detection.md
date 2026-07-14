# HAi Anomaly Detection

## Details

The details section allows you to define the criteria that will be used to identify anomalies in request records. Each rule is made up of a set of conditions that must be met for a request to be considered an anomaly.

* **Service**: The service to which the requests belong.
* **Catalog**: The request catalog to which the requests belong.
* **Raised within**: The time period in which the requests must occur to be considered part of the same cluster.
* **Request Type**: The type of requests to include in the cluster.

## Clustering

Clustering is the process of grouping similar requests together based on their attributes. This allows HAi to identify patterns and trends in the data, which can be used to detect anomalies.

* **Number of Requests**: The number of requests within a cluster before an event is created.
* **Automatically Raise Request**: If an anomaly is detected, HAi can automatically raise a request to notify the appropriate team or individual. The request will contain details about the anomaly, including the affected service and any relevant information from the clustered requests.
* **Notify**: If an anomaly is detected, HAi can send a notification to the appropriate team. The notification will contain details about the anomaly, including the affected service and any relevant information from the clustered requests.

## Raising Request

If an anomaly is detected, HAi can automatically raise a request to notify the appropriate team or individual. The request will contain details about the anomaly, including the affected service and any relevant information from the clustered requests.
