# Data Access Rules Help

Data access rules allow you to define a set of criteria that will restrict all AI processing against either a Request or a Knowledge Article, each have their own set or rules called a ```Rule Set```.

The rules are processed one at a time in order from the first down, if a rule is evaluated to true then access is restricted and AI will not be processed.

## Rule Sets

The rules are split into Rule Sets, each allowing for a customizable list of rules:

- Request - Restricts HAi against Requests, based on the available Entity rules.
- Knowledge - Restricts HAi against Knowledge Articles, based on the available Entity rules.

| **Rule Set** | **Entity**    | **Rule Types** |
|--------------|---------------|----------------|
| Request      | Service       | Is / Is Not    |
| Request      | Company       | Is / Is Not    |
| Request      | Team          | Is / Is Not    |
| Knowledge    | KnowledgeBase | Is / Is Not    |

## Examples

Example 1 - Block access for requests logged against a specific service (HR Grievance, ID 1203):

- **Rule Set** Request
- **Entity** Service
- **Types** Is
- **EntityId** 1203

Example 2 - Block access for requests logged against any service that isn't Desktop Support (ID 1008):

- **Rule Set** Request
- **Entity** Service
- **Types** Is Not
- **EntityId** 1008

Example 3 - Allow only 1st Line Support Team (ID 1stLineSupport), but also block any requests that are against the Organization Acme Inc (ID 129):

- Rule 1
  - **Rule Set** Request
  - **Entity** Team
  - **Types** Is Not
  - **EntityId** 1stLineSupport
- Rule 2
  - **Rule Set** Request
  - **Entity** Service
  - **Types** Is
  - **EntityId** 129
  