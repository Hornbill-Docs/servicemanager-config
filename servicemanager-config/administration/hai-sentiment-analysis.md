---
layout: article-toc
---
# Sentiment Analysis Configuration

::: important
HAi features are currently in a closed beta. You can only access these features after you register. Contact your Hornbill Customer Success representative to join the program.
:::

## Before you begin

Ensure you have [enabled HAi features](/servicemanager-config/administration/hai). You can customize how much data the system uses and which timeline update types trigger a request summary. To manage these settings, navigate to the [application settings](/servicemanager-config/advanced-tools-and-settings/application-settings) for Service Manager.

| Setting | Description |
| :-- | :-- |
| `generativeAi.sentimentAnalysis.availablePostTypes` | Determines the types of posts used to generate the request sentiment. Valid values include: `Authorization`, `Customer`, `Email`, `Escalate`, and `update`. |
| `generativeAi.sentimentAnalysisAutoUpdates` | Enables or disables automatic request sentiment analysis when a customer provides an update. |

## Auto updates

When you enable `Auto Updates`, the system checks the sentiment of a request if the person posting or commenting is the customer associated with that request. This applies to the following scenarios:

* **Customer Portal:** The customer adds a timeline post or comment.
* **Employee Portal:** The customer adds a timeline post or comment.
* **Email Auto Responder:** The system updates a request via an email sent by the customer.
* **Mailbox:** A user applies an email to a request where the sender is the customer.

## Data processing

When the system performs a sentiment analysis, it processes specific data from the active request.

### Request fields

The following technical fields are processed:

* `h_itsm_requests.h_description`
* `h_itsm_requests.h_summary`
* `h_itsm_requests.h_fk_user_name`

### Timeline data

The system filters the request timeline using the following criteria: `["Customer","Email","update"]`. For every post in the filtered timeline, the system sends the following data:

* `actorInfo.name`
* `content`

For any comments associated with these filtered posts, the system sends:

* `actorInfo.name`
* `comment`

### Custom questions

The system passes the first 100 custom questions. It excludes `file-upload` and `label` types. The data is paired using the following format:

* `h_question`
* `h_answer_value`
