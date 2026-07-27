# HAi Settings

## HAi Providers

By enabling any of these optional HAi features, you are agreeing to allow a third party to process your data ([HAi Providers](/servicemanager-config/administration/hai-providers)). Data from prompts and underlying request data is passed to a HAi Provider using encrypted connections. See [HAi Providers](/servicemanager-config/administration/hai-providers) for further details.

## HAi Features

Each of the following HAi features can be enabled or disabled independently. When enabled, the feature will process data from the request you are in and send it to a HAi Provider for processing.

* **Request Summarizer**: Generates a summary of a request based on the request description, timeline posts, comments, and custom questions. The summary is generated when a request is created or updated.
* **Sentiment Analysis**: Analyzes the sentiment of a request based on the request description, timeline posts, comments, and custom questions. The sentiment is generated when a request is created or updated.
* **Text Assist**: Provides text assistance for a request based on the request description, timeline posts, comments, and custom questions. The assistance is generated when a request is created or updated.
* **Knowledge Generator**: Generates a knowledge draft from a resolved or closed request based on the request description, timeline posts, comments, and custom questions. The knowledge draft is generated when a request is resolved or closed.
* **Suggest Resolution**: Suggests a resolution for a request based on the request description, timeline posts, comments, and custom questions. The suggestion is generated when a request is created or updated.
* **Email Processing**: Processes incoming emails and extracts relevant information to create or update requests. The processing is done when an email is received.
* **Email Attachment Labeling**: Labels email attachments based on their content and context. The labeling is done when an email is received.

## Auto Updates

Some features provide Auto Updates, which means that the feature will automatically generate content. See the documentation on each feature for more information on what triggers an auto update.

## Data processing

The following areas of functionality send request data during each invocation and are documented as follows:

### Request Summarizer

When summarizing a request the following data from the request you are in is processed:

* `h_itsm_requests.h_description`
* `h_itsm_requests.h_summary`
* `h_itsm_requests.h_fk_user_name`

The timeline of the request is filtered down with the following filters '["Authorization","Customer","Email","Escalate","update"]' and can be updated [here](/servicemanager-config/administration/hai-request-summariser).

Each post in the timelines sends the following

* `actorInfo.name`
* `content`

Each comment associated to any filtered posts in the timelines sends the following

* `actorInfo.name`
* `comment`

Custom Questions (first 100) are passed, excluding the type `file-upload` and `label` and are paired with the question text as follows:

* `h_question`
* `h_answer_value`

Completed Tasks information as follows:

* `title`
* `category`
* `owner`
* `outcome`
* `completed on`
* `details`
* `assigned`
* `reference`

### Suggest Resolution

When suggesting a resolution against a request the following data from the request you are in is processed:

* `h_itsm_requests.h_description`
* `h_itsm_requests.h_summary`
* `h_itsm_requests.h_fk_username`

The timeline of the request is filtered down with the following filters '["Update","Email","Customer"]'

Each post in the timelines sends the following

* `actorInfo.name`
* `content`

Each comment associated to any filtered posts in the timelines sends the following

* `actorInfo.name`
* `comment`

### Knowledge Draft

When generating a knowledge draft from a resolved or closed request the following data is sent:

* `h_itsm_requests.h_description`
* `h_itsm_requests.h_summary`
* `h_itsm_requests.h_resolution`

### Text Assist

Text assist combined with snippets or used within a workflow and passing in variables can pass any data a user has selected to pass to a [HAi Provider](/servicemanager-config/administration/hai-providers). Nothing is sent automatically. In the case of snippets, when the snippet is selected the analyst will see the data before the text is passed as part of the prompt when using Text Assist after a snippet.

### Sentiment Analysis

When the system performs a sentiment analysis, it processes specific data from the active request.

#### Request fields

The following technical fields are processed:

* `h_itsm_requests.h_description`
* `h_itsm_requests.h_summary`
* `h_itsm_requests.h_fk_user_name`

#### Timeline data

The system filters the request timeline using the following criteria: `["Customer","Email","update"]`. For every post in the filtered timeline, the system sends the following data:

* `actorInfo.name`
* `content`

For any comments associated with these filtered posts, the system sends:

* `actorInfo.name`
* `comment`

#### Custom questions

The system passes the first 100 custom questions. It excludes `file-upload` and `label` types. The data is paired using the following format:

* `h_question`
* `h_answer_value`
