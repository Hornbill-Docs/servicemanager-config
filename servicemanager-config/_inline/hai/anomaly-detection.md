# Anomaly Detection

Anomaly Detection uses HAi to automatically identify patterns in request records that might indicate a potential issue with a service.

## Rules

Rules are used to define the criteria that will be used to identify anomalies in request records. Each rule is made up of a set of conditions that must be met for a request to be considered an anomaly.

* The number of requests within a cluster before an event is created.
* The time period in which the requests must occur to be considered part of the same cluster.
* The type of requests to include in the cluster.
* The service to which the requests belong.
