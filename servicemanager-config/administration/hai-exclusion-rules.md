---
layout: article-toc
---

# Exclusion rules

Exclusion rules allow you to define a set of criteria that will restrict all AI processing against either a Request or a Knowledge Article; each has its own set of rules called a Rule Set.

## Rule Sets

The rules are split into Rule Sets, each allowing for a customizable list of rules:

* **Request**: Restricts HAi against Requests, based on the available Entity rules.
* **Knowledge**: Restricts HAi against Knowledge Articles, based on the available Entity rules.

The list will show either request sets or knowledge sets based on the selected Rule Set filter.

|Rule Set|Entity|Rule Types|
|---|---|---|
|Request|Service|Is equal to / does not equal / is one of / is not one of|
|Request|Company|Is equal to / does not equal / is one of / is not one of|
|Request|Team|Is equal to / does not equal / is one of / is not one of|
|Knowledge|KnowledgeBase|Is equal to / does not equal / is one of / is not one of|

### Rule options

* **Rule Set**: The Rule Set to which the rule belongs, either Request or Knowledge.
* **Name**: The name of the rule, this is for your reference only.
* **Entity**: The Entity to which the rule applies, either Service, Company, Team or KnowledgeBase.
* **Operator**: The operator to use for the rule.
* **Select `entity name`**: The values to which the rule applies, based on the selected Entity. This will display either Service, Company, or Team.

Example exclusion rule.  This rule will exclude the use of AI on a request for any team that is not 1st Line Support, 2nd Line, Change Management, or Problem Management.

![Exclusion rule form](/_books/servicemanager-config/administration/images/hai-exclusion-rule-form.png)

## Test

A test option is available to allow you to test your rules against a Request or Knowledge Article.  You will be prompted to enter either the Request ID or Knowledge Article ID to test, depending on the Rule Set you are testing.  

This will return a result of either **Success** where HAi can be used on the selected entity or **Warning** which indicates that HAi can't be used on the entity.

![Exclusion rule test result](/_books/servicemanager-config/administration/images/hai-exclusion-test-result.png)
