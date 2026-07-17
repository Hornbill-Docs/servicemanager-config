# Import Supplier Contacts

You can import supplier contacts into Service Manager using a CSV file. The CSV file must contain the following columns:

- `Contact Name`
- `Contact Email`
- `Contact Phone`

| Field | Description |
| --- | --- |
| Supplier Contact Id | The unique identifier (primary key) for the specified supplier contact, e.g. 100001. If this value is provided, the existing supplier contact will be updated. If it is left empty, a new supplier contact will be created (providing a valid supplier has been specified) |
| Supplier | The name of the existing supplier. This must be provided if you are attempting to create a new supplier contact. If you are updating an existing supplier contact by providing a supplier contact id, this field will be ignored |
| First Name | The first name of the supplier contact (100 characters) |
| Last Name | The last name of the supplier contact (100 characters) |
| Job Title | The job title of the supplier contact (100 characters) |
| Email Address | The primary email address of the supplier contact (100 characters) |
| Email Address 2 | The secondary email address of the supplier contact (100 characters) |
| Email Address 3 | Any additional email address for the supplier contact (100 characters) |
| Phone Number | The primary phone number of the supplier contact (32 characters) |
| Phone Number 2 | The secondary phone number of the supplier contact (32 characters) |
| Phone Number 3 | Any additional phone number for the supplier contact (32 characters) |
| Language | The language of the supplier contact, e.g en-GB |
| Country | The country of the supplier contact, eg. GB |
| Notes | A freetext field for additional notes about the supplier contact |
| Status | The status of the supplier contact. Accepted values are (status.active, status.archived). If no value is provided, status.active will be used |
| Custom 0 | Additional data mapped to custom fields (255 characters) |
| Custom 1 | Additional data mapped to custom fields (255 characters) |
| Custom 2 | Additional data mapped to custom fields (255 characters) |
| Custom 3 | Additional data mapped to custom fields (255 characters) |
| Custom 4 | Additional data mapped to custom fields (255 characters) |
| Custom 5 | Additional data mapped to custom fields (255 characters) |

