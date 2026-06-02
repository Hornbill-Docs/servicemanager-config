---
layout: article-toc
---

# Asset Depreciation

An asset depreciation calculator is available that helps determine the loss of value over time for your assets.  This calculator uses a set of fields to calculate the current value of an asset based on its original value, start date, and expected lifespan. You can use this information to make informed decisions about asset replacement and budgeting.

![Asset depreciation calculator](/_books/servicemanager-config/images/asset-depreciation-calculator.png)

## Required fields

In order to make the asset depreciation calculator available to users, you need to start by adding the required fields to the asset types that you want it to be available for. Then each of these fields must be filled in for an asset in order for the calculator to be visible.

* **Cost**: The original cost of the asset when it was purchased. This is a crucial input for calculating depreciation, as it serves as the starting point for determining the asset's value over time.
* **Depreciation Method**: The method used to calculate the asset's depreciation over time. Methods include straight-line and reducing balance. The choice of method will determine if the depreciation value is calculated as a fixed amount or as a percentage of the asset's remaining value.
* **Depreciation Value (percentage or amount)**: The amount by which the asset's value decreases over time. If the depreciation method is straight-line, this will be a fixed amount. If the method is reducing balance, this will be a percentage of the asset's remaining value.
* **Depreciation Frequency (months)**: The interval at which depreciation is calculated.
* **Depreciation Start Date**: The date when the asset's depreciation calculations begin.
* **Depreciation Term (months)**: The total duration over which the asset will be depreciated.

## Optional fields

These fields are not required to use the asset depreciation calculator, but they can provide additional context and information about the asset's value over time:

* **Currency**: The currency in which the asset's value is expressed.
* **Residual Value**: The estimated value of the asset at the end of its useful life. This field is not directly linked to the calculator, but it can be used to manually enter the final value in the depreciation schedule.  
* **Depreciation Date**: The date when the asset's depreciation is calculated. This field is not directly linked to the calculator, but it can be used to manually enter the date of the most recent depreciation calculation.

## Adding the required fields to an asset type

In order for asset users to populate the required fields for the asset depreciation calculator, you need to add these fields to the asset type. This is typically done under the **Detail Fields** tab of the asset type configuration. You can choose to add these fields to the **Summary Fields** view as well.

1. Navigate to **Configuration > Service Manager > Assets > Manage Types**.
2. Select the asset type you want to edit from the left-hand menu.
3. Go to the **Detail Fields** tab.
4. Select the **Common field** option and use the filter to find the required fields and select the field to add it.  If they are not in the list, this means they have already been added.

Once added to the detail fields you can move the fields under the appropriate section header such as **Financial Information**. This will help users find the fields when they are editing an asset. Optionally, you can add a new section header called **Depreciation** to group the required fields together.
