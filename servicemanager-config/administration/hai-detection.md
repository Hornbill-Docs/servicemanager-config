# HAi Detection

## Before you begin

* HAi features are currently in a closed beta. You can only access these features if you are part of the beta program. Contact your Hornbill customer success representative for more information.

## Overview

A HAi Detection rule analyzes requests across a set of conditions. When these conditions are met, HAi Detection creates a new event. 

An event can trigger a new request and an in-app notification to supporting teams. 

Events are a useful way surfacing issues that arise across the service desk, that might otherwise go unnoted. They are also helpful for identifying and managing major incidents.

Events are defined and configured by creating a new HAi Detection rule.

## Details

The details section allows you to define the criteria that will be used to identify events in request records. Each rule is made up of a set of conditions that must be met for a request to contribute to an event.

* **Service**: The service to which the requests belong.
* **Catalog**: The request catalog to which the requests belong.
* **Raised within**: The time period in which the requests must occur to be considered part of the same cluster.
* **Request Type**: The type of requests to include in the cluster.

## Clustering

Clustering is the process of grouping similar requests together based on their attributes. This allows HAi to identify patterns and trends in the data, which can be used to detect events.

* **Number of Requests**: The number of requests within a cluster before an event is created.
* **Automatically Raise Request**: If an event is detected, HAi can automatically raise a request to notify the appropriate team or individual. The request will contain details about the event, including the affected service and any relevant information from the clustered requests. The new request acts as a parent request to the events in the event cluster.
* **Notify**: If an event is detected, HAi can send a notification to the appropriate team. The notification will contain details about the event, including the affected service and any relevant information from the clustered requests.

## Raising Request

If an event is detected, HAi can automatically raise a request to notify the appropriate team or individual. The request will contain details about the event, including the affected service and any relevant information from the clustered requests.
