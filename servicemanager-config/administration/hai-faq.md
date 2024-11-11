---
title: Hornbill AI FAQ
description: This guide covers the frequently asked questions of HAi (Hornbill AI).
coverImage: /_books/servicemanager-config/administration/images/hai-cover.jpg
layout: article-toc
---

# Hornbill AI FAQ's

## FAQ

**Q: What types of data are required for Hornbill AI?**
**A:** Data inputs for HAi can be categorized into two areas:

1. Text inputs from an input field, these are primarily for [Text Assist](/servicemanager-user-guide/hai/text-assist) prompts and only use the data in the text felid or highlighted text before the prompt is requested.
2. Prompts that pass business data not directly input by a user, all of these are [documented](/servicemanager-config/administration/hai#data) and can be disabled separately from Text Assist. The only type of personal data passed is Name, this is used to differentiate updates on request timelines for the purposes of summarization.

**Q: What output does Hornbill AI produce?**

**A:** Currently only generated text is produced by Hornbill AI, no analysis or trends or identification is performed.

**Q: Are the inputs or outputs used for Training?**

**A:** Only by Hornbill and not by any Third Party AI Providers, as documented in the [Hornbill Artificial Intelligence Agreement](https://www.hornbill.com/hubfs/Website/PDF/HAI%20Agreement.pdf) inputs and outputs will be used by the Hornbill AI team to develop internal models for future customer functionality, these will have a fully transparent process for how the training data is uses and the processes involved to remove personal or identifiable data, anonymising and addressing bias before the models are made available to customers. As stated in the agreement customers can opt out of this at any time and any data already used for training will be removed.

**Q: Are their any restrictions on the use of Hornbill AI?**

**A:** Any restriction on the use of Hornbill AI is defined in section 5 of the [Hornbill Artificial Intelligence Agreement](https://www.hornbill.com/hubfs/Website/PDF/HAI%20Agreement.pdf) and any relevant [AI Supplier Terms](/servicemanager-config/administration/hai-usage-policy#third-party-terms)

**Q: Does Hornbill have any access to the inputs or outputs of Hornbill AI?**

**A:** Anonymized access to the logs by the Hornbill AI Team is [detailed here](/servicemanager-config/administration/hai-logs#monitoring-of-logs).

**Q: What measures are in place to protect the privacy and security of Hornbill AI inputs and outputs?**

**A:** Hornbill AI Audit logs are stored on the customer instance and all security and encryption is covered by our ISO 27001 and 27008 accreditation's, details on these and our data center security can be found on [Hornbill Trust](https://trust.hornbill.com/compliance/)

Details on audit log storage is [detailed here](/servicemanager-config/administration/hai-logs#monitoring-of-logs).

Data is passed to an [HAi Provider](/servicemanager-config/administration/hai-providers) (Azure, OpenAI) via encrypted SSL connections only .

**Q: Who owns the rights to the input and outputs of Hornbill AI?**

**A:** The customer owns 100% rights to the input and output of Hornbill AI that are logged in the HAi Audit Logs made up of user imputed data or business data passed, System Prompts that make up the generative AI Functionality are proprietary to Hornbill and as such not covered by this and are not logged in the HAi Audit Logs.

**Q: How does Hornbill identify and manage potential issues or risks with the validity and reliability of the output?**

**A:** Out of the box Hornbill AI functionality is regularly tested especially when new [models are available](https://www.hornbill.com/blog/how-the-hai-lab-team-test-new-genai-models-like-gpt-4o) for the quality and accuracy of the output. The risks are detailed in section 4 of the [Hornbill Artificial Intelligence Agreement](https://www.hornbill.com/hubfs/Website/PDF/HAI%20Agreement.pdf) and Hornbill is constantly monitoring and reviewing advancements in AI especially Generative AI for new or emerging risks and if appropriate how to they can be mitigated.