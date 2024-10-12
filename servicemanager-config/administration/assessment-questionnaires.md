---
layout: article-toc
---
# Questionnaires
Assessment questionnaires are a collection of questions that can be created and presented in the Assessment tab of a request. Rather than having someone assume or apply their perception of the level, the questions can present criteria to make that decision.

## How To Access
Assessment questionnaires are defined under the Service Manager configuration.
1. On the keyboard use the key combination `Ctrl+Shift+s`.
1. Search [Configuration](/esp-config/getting-started/using-configuration) for *Assessment*.
1. In the results list select `Assessments`.
1. Select the `Assessments` tab.

or

1. Open configuration and select `Service Manager` from the navigation dropdown.
2. In the navigation panel locate the section titled *Administration*.
3. Select `Assessments`.
4. Select the `Assessments` tab.

### Questions
One or more questions can be created for each assessment. Once a question has been created, multiple answers can be defined and will allow the user to select the most suitable answers when running through the assessment.

### Answers
Each question requires one or more answers to be created. Answers are presented to a user as a list of single select radio buttons, only allowing one answer to be selected per question. Each answer provides a weight level. This is a value that will be used at the end of the assessment to determine the level to be applied. The weight levels for all the selected answers are totaled up and the thresholds are then used to determine the level.

* **Answer**<br>Write an answer to the question that you have provided.
* **Weight**<br>Enter a numerical value that will represent the weight level for this answer.
* **Language**<br>Translations into other languages can be provided for each answer.
* **Thresholds**<br>The Thresholds determine which level is set against a request. This is based on an lower and upper limit for each level where the numbers are calculated against the total value of all the weighting level of all the answered questions.

### Level
The available levels that have been defined will be available as part of the thresholds. Additional levels can be added from the levels option for both impact and urgency.
### Lower Limit
The lower limit specifies that this level will be applied if the total of the weighting from all the answers are above this number but below the upper limit.
### Upper Limit
The upper limit specifies that this level will be applied if the total of the weighting from all the answers are below this number but above the lower limit.
### Auto-set
Provided that there is more than one answer to one or more questions where a weighting level has been specified, clicking on the `Auto-set` button will equally divide up the lowest possible limit with the highest possible limit across the different available impact levels. Depending on the number of answers that have been defined with a weight value, the results of an Auto-set may still need to be adjusted so that there is no overlap between levels.

<!-- workflow 
Multiple assessments can be created and then each assessment individually used within a BPM workflow and presented to a user at an appropriate time in the process.
-->

<!-- https://wiki.hornbill.com/index.php?title=Service_Manager_Assessments>