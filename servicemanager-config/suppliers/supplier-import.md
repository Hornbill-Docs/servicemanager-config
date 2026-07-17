---
draft: true
---

# Import Suppliers

There are three types of supplier imports that can be performed in Service Manager:

## Template files

Each type of import has a template file that can be downloaded from the Service Manager interface. These template files contain the required columns and formatting for each type of import.

## Import suppliers

You can import suppliers into Service Manager using a CSV file. The CSV file must contain the following columns:

- `Name`

|Field|Description|
|---|---|
|Name|The name of the new supplier (255 characters)|
|Status|The status of the new supplier. Accepted values are (status.active, status.preferred, status.barred, status.archived). If no value is provided, status.active will be used.|
|Supplier Status|The supplier status of the new supplier. Accepted values can be found in the simple list 'Supplier Statuses' which can be viewed under 'Hornbill Supplier Manager > Simple Lists'|
|Industry|The industry of the new supplier. Accepted values can be found in the simple list 'Industry' which can be viewed under 'Hornbill Collaboration > Simple Lists'|
|Email Address Accounts|The email address of the accounts team for the new supplier (100 characters)|
|Email Address Sales|The email address of the sales team for the new supplier (100 characters)|
|Email Address Support|The email address of the support team for the new supplier (100 characters)|
|Address|The address of the new supplier (255 characters)|
|City|The city the new supplier is primarily based in (255 characters)|
|State|The state the new supplier is primarily based in (255 characters)|
|Postal Code|The postal code of the address where the new supplier is primarily based (16 characters)|
|Country|The country the new supplier is primarily based for example 'GB' (255 characters)|
|Timezone|The timezone the new supplier is primarily based in, e.g. GMT Standard Time|
|Phone Number|The primary phone number of the new supplier (32 characters)|
|Website|The main website of the new supplier (255 characters)|
|Notes|Any additional notes about the new supplier (no character limit)|
|Owner|The user id of the supplier owner (leave blank if this is the same user performing the import)|
|Permissions|Permission records separated by commas. For users: 'user:' + user id. For groups: 'group:' + group id. For roles: 'role:' + role name.|
|Custom 0|Additional data mapped to custom fields|
|Custom 1|Additional data mapped to custom fields|
|Custom 2|Additional data mapped to custom fields|
|Custom 3|Additional data mapped to custom fields|
|Custom 4|Additional data mapped to custom fields|
|Custom 5|Additional data mapped to custom fields|
|Custom 6|Additional data mapped to custom fields|
|Custom 7|Additional data mapped to custom fields|
|Custom 8|Additional data mapped to custom fields|
|Custom 9|Additional data mapped to custom fields|

