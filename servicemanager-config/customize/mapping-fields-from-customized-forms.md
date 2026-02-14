# Mapping Fields from Customized Forms

Any information captured in customized forms results in the question and answer being visible on the request form in a Questions collapsible section. Custom forms also support field mapping which is a mechanism that allows us to write the information to the main request table.

Why would I use field mapping?
Field mapping is desirable for two reasons:

1. Make the answers to custom questions more accessible for reporting (i.e. Measures, Widgets, Reports).
2. Make the answers to custom questions available in email templates.

The information gathered in a capture custom form is stored in a table h_itsm_questions and is intended to act as a sort of audit history displaying what information was provided at the point the request was logged. Answers in the Questions section of a request can be edited. This option is only available for single-line and multi-line text fields and only for users having "Service Manager Delete Questions" or "Service Desk Admin" roles. Any other type of answer cannot be edited.

The way the data is stored in the table h_itsm_questions does not offer us much flexibility when it comes to reporting and also means is not accessible via the email template variable picker. The exercise of field mapping ensures the data is written to h_itsm_requests (the main request table) which means it is readily available.

## Configuring a Custom Field for Mapping

When creating a custom question on a customized form, each question requires a Field ID and it is here that the mapping can be performed. When defining the Field ID, if you use any of the following values, the answer to this question will be mapped to the database column you have specified.

![Custom Form Field Settings](/_books/servicemanager-config/customize/images/custom-form-field-settings.png
)

Field mapping takes place when a supported database column name is specified as the field ID of a custom field.

### Which Database Columns Support Field Mapping?

To map a custom form answer to one of the supported database columns, the form field ID needs to be set using the following format h_custom_a or the appropriate column you would like to map to. The table below lists all the database columns that support field mapping and the type of content that they can hold.

| Available Columns | Data Type/Capacity | Description |
|---|---|---|
| **h_summary** | VARCHAR/255 characters | The Summary field of a request  |
| **h_description** | TEXT/unlimited* | The description field of a request  |
| **h_site** | VARCHAR/64 characters | The site field for a request  |
| **h_custom_a - h_custom_o** | VARCHAR/255 characters | VARCHAR custom fields a - o each suitable for holding up to 255 characters of any type.  |
| **h_custom_p - h_custom_t** | TEXT/unlimited* | TEXT custom fields p - t each suitable for holding large amounts of text characters of any type.  |
| **h_custom_21 - h_custom_25** | DATETIME/a single date-time stamp | DATETIME custom fields 21 - 25 each suitable for holding a single date-time stamp (YYYY-MM-dd HH:mm:ss). These columns should ONLY be used in conjunction with a date-time picker.  |
| **h_custom_26 - h_custom_30** | INTEGER/any whole number | INTEGER custom fields 26 - 30 each suitable for holding whole numbers. When mapping to these columns, ensure the following RegEx is specified in your Custom field settings: [0-9]<br>Note: Phone numbers are not Integers, do not use these fields to store phone numbers. |
| **h_custom_31 - h_custom_40** | TEXT/unlimited* | TEXT custom fields 31 - 40 each suitable for holding large amounts of text characters of any type.  |
| **h_backout_plan** | Text/Unlimited* | The Back Out Plan of a Change or Release Request  |
| **h_support_plan** | Text/Unlimited* | The Support Plan of a Change or Relase Request  |
| **h_communication_plan** | Text/Unlimited* | The Communication Plan of a Change or Release Request  |
| **h_test_plan** | Text/Unlimited* | The Test Plan of a Change or Release Request  |
| **h_implementation_plan** | Text/Unlimited* | The Implementation Plan of a Change or Release Request  |
| **h_security_implication** | Text/Unlimited* | The Security Implications of a Change or Release Request  |
| **h_change_justification** | Text/Unlimited* | The Change Justification a Change Request  |
| **h_release_justification** | Text/Unlimited* | The Change Justification a Release Request  |
| **h_disruption_level** | VarChar/255 Characters | The Disruption Level of a Change or Release Request  |
| **h_change_category** | VarChar/100 Characters | The Category of a Change Request  |
| **h_release_category** | VarChar/100 Characters | The Category of a Release Request  |
| **h_proposed_start_time** | DATETIME/a single date-time stamp | The Proposed Start date/time of the a Change or Release Request - (YYYY-MM-dd HH:mm:ss). These columns should ONLY be used in conjunction with a date-time picker  |
| **h_proposed_end_time** | DATETIME/a single date-time stamp | The Proposed End date / time of the a Change or Release Request - (YYYY-MM-dd HH:mm:ss). These columns should ONLY be used in conjunction with a date-time picker  |
| **h_workaround** | Text/Unlimited* | The Workaround for a Problem or Known Error record |
| **h_change_type** | VarChar/128 Characters | A [simple list (changeRequestType)](/servicemanager-config/setup/service-manager-simple-lists) is used to select the change type when manually selecting the type.  Values used when mapping should match those in the simple list |
| **h_release_type** | VarChar/128 Characters | A [simple list (releaseRequestType)](/servicemanager-config/setup/service-manager-simple-lists) is used to select the release type when manually selecting the type.  Values used when mapping should match those in the simple list |

unlimited* - TEXT fields have a maximum capacity of 65000 characters.

### Considerations

* When specifying the column you wish to map to in your custom form id, this value is case sensitive. e.g. h_summary will achieve the desired mapping but h_Summary will fail to pull any values through. Ensure that the mapped value is written in lowercase.
* When the option of value/display is offered (e.g. in a static drop-down list) it is the display value that will be mapped to the column.
* Do not store Telephone Numbers in Integer fields. At best you will lose the initial '0', even more likely is that the value will exceed the maximum allowed for an Integer and the operation will fail.
* If the Default Request Details form is used in your Intelligent Capture flow, and you try to map to h_summary or h_description, the values will not overwrite or be written to the summary or description fields i.e. the standard "Request Details" form takes precedence, but the custom questions and answers will still be written to the Questions section on the request.
* If the same mapping is used on different custom forms in your Intelligent Capture flow, the first mapping will be written to the specified default field on the request, and any subsequent mapping to the same field will not overwrite this value, but will be written to the Questions section on the request.
* When custom questions have been mapped, the question and answer are still available in the Questions section on a request as well as now being available in the mapped field. This restriction can be controlled via the application setting "guest.itsm.progressiveCapture.overwriteCustomFieldValue".
* Once you have configured field mapping in your Intelligent Capture custom forms, you may need to expose the mapped field on the request. See the Request Details Form Designer for more information.
* When creating your email template simply look for the custom options available from the variables drop-down pick list. Selecting the required variable in your email template, will pass through the answer from your custom question which has been mapped to the corresponding custom field.
