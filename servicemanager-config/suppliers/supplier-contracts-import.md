# Import Supplier Contracts

You can import supplier contracts into Service Manager using a CSV file. The CSV file must contain the following columns:

- `Contract Name`
- `Supplier ID`

| Field | Description |
| --- | --- |
| Supplier Contract Id | The unique identifier (primary key) for the specified supplier contract, e.g. C20200100001. If this value is provided, the existing supplier contract will be updated. If it is left empty, a new supplier contract will be created (providing a valid supplier has been specified) |
| Supplier | The name of the existing supplier. This must be provided if you are attempting to create a new supplier contract. If you are updating an existing supplier contract by providing a supplier contract id, this field will be ignored |
| Name | The name of the supplier contract (255 characters) |
| Description | A description of the supplier contract (512 characters) |
| Type | The type of the supplier contract. Accepted values can be found in the simple list 'Supplier Contract Types' which can be viewed under 'Hornbill Supplier Manager > Simple Lists' |
| Start Date | The start date of the supplier contract. Must be in format YYYY-MM-DD HH:MM:SS |
| End Date | The end date of the supplier contract. Must be in format YYYY-MM-DD HH:MM:SS |
| Renewal Start Date | The renewal start date of the supplier contract. Must be in format YYYY-MM-DD HH:MM:SS |
| Renewal End Date | The renewal end date of the supplier contract. Must be in format YYYY-MM-DD HH:MM:SS |
| Currency | The currency of the supplier contract, e.g. £ or $ |
| Value | The numerical value of the supplier contract |
| Acquisition Method | The acquisition method of the supplier contract. Accepted values can be found in the simple list 'Supplier Contract Acquisition Methods' which can be viewed under 'Hornbill Supplier Manager > Simple Lists' |
| Cancelation Notice Period | The cancelation notice period of the supplier contract |
| Cost Center | The cost center of the supplier contract |
| Invoice Number | The invoice number of the supplier contract |
| Order Number | The order number of the supplier contract |
| Payment Type | The payment type of the supplier contract. Accepted values can be found in the simple list 'Supplier Contract Payment Types' which can be viewed under 'Hornbill Supplier Manager > Simple Lists' |
| Status | The status of the supplier contract. Accepted values are (status.active, status.archived, status.draft). If no value is provided, status.active will be used |
| Sub Status | The sub status of the supplier contract. Accepted values can be found in the simple list Supplier Contract Sub Status |
| Owner | The user id of the owner of the supplier contract. |
| Budget Owner | The user id of the budget owner of the supplier contract. |
| Business Owner | The user id of the business owner of the supplier contract. |
| Working Time Calendar | The working time calendar that will run against the supplier contract. Values can be found in the Admin Tool under Home - System - Working Time Calendars. An example would be the Hornbill Service Manager calendar: ServiceDeskDefaultCalendar |
| Target Minutes Per Event | The number of target minutes for each event. 4 hours for example is 240 |
| Agreed Compliance Target Percentage | The agreed percentage number, for example: 90 |
| Contact Email Address | The email address that should be used in correspondence with the supplier during an event |
| Penalty Description | A description of any penalties the supplier will face for breaching their contract (1024 characters) |
| Notes | Any additional notes about the new supplier contract (no character limit) |
| Custom 0 | Additional data mapped to custom fields (255 characters) |
| Custom 1 | Additional data mapped to custom fields (255 characters) |
| Custom 2 | Additional data mapped to custom fields (255 characters) |
| Custom 3 | Additional data mapped to custom fields (255 characters) |
| Custom 4 | Additional data mapped to custom fields (255 characters) |
| Custom 5 | Additional data mapped to custom fields (255 characters) |
| Custom 6 | Additional data mapped to custom fields (255 characters) |
| Custom 7 | Additional data mapped to custom fields (255 characters) |
| Custom 8 | Additional data mapped to custom fields (255 characters) |
| Custom 9 | Additional data mapped to custom fields (255 characters) |
| Custom 10 | Additional data mapped to custom fields (255 characters) |
| Custom 11 | Additional data mapped to custom fields. Must be in format YYYY-MM-DD HH:MM:SS |
| Custom 12 | Additional data mapped to custom fields. Must be in format YYYY-MM-DD HH:MM:SS |
| Custom 13 | Additional data mapped to custom fields. Must be in format YYYY-MM-DD HH:MM:SS |
| Custom 14 | Additional data mapped to custom fields. Must be in format YYYY-MM-DD HH:MM:SS |
| Custom 15 | Additional data mapped to custom fields. Must be in format YYYY-MM-DD HH:MM:SS |
| Custom 16 | Additional data mapped to custom fields (Integer) |
| Custom 17 | Additional data mapped to custom fields (Integer) |
| Custom 18 | Additional data mapped to custom fields (Integer) |
| Custom 19 | Additional data mapped to custom fields (Integer) |
| Custom 20 | Additional data mapped to custom fields (Integer) |
| Custom 21 | Additional data mapped to custom fields (Decimal) |
| Custom 22 | Additional data mapped to custom fields (Decimal) |
| Custom 23 | Additional data mapped to custom fields (Decimal) |
| Custom 24 | Additional data mapped to custom fields (Decimal) |
| Custom 25 | Additional data mapped to custom fields (Decimal) |