---
title: Hornbill AI Automations
description: Automate your workflow with HAi Automations in Hornbill! Utilize the Summarize Request task to easily summarize requests triggered from workflows. Update the request timeline and access the summary as a variable for future processes. With the askHAi task, generate clarifying questions based on initial request details. Ensure validation before direct user communication and integrate responses into timelines. Enhance your automation capabilities with Hornbill AI.
coverImage: /_books/servicemanager-config/administration/images/hai-cover.jpg
layout: article-toc
---
# HAi Automations
## Summarize Request
Using the Requests entity in Hornbill Automations and selecting the Type HAi you will find the Summarize Request task, like the UI for summarizing the request. The only difference here is it being triggered from a workflow. Optionally you can update the request timeline. The summary is also returned as a variable for use in the process later on.
<img src="/_books/servicemanager-config/administration/images/hai-automation-summaize.png" alt="Hornbill AI Summarize Request - Automation" ></img>


## askHAi
Using the Requests entity in Hornbill Automations and selecting the Type HAi you will find the askHai task. This allows fairly open prompts to be used as part of a Hornbill Workflow. The following example uses the initial summary and description of a request and asks for some clarifying questions to be generated if possible. It's important to not directly send this straight to a user in the first instance and validate its output. As with other automations, the response is optionally added to the timeline and is also returned as a variable for use in the process later on.

<img src="/_books/servicemanager-config/administration/images/hai-automation-ask.png" alt="Hornbill AI askHai - Automation" ></img>
<img src="/_books/servicemanager-config/administration/images/hai-automation-ask-2.png" alt="Hornbill AI askHai - Automation" ></img>
