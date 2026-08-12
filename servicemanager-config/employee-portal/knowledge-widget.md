# Knowledge Base Articles Widget

The Knowledge Articles widget lets Employee Portal users search and open published knowledge articles that are available to them. It can be configured to include selected knowledge bases and selected article types.

![Knowledge articles widget screenshot](/_books/servicemanager-config/employee-portal/images/knowledge-widget.png)

## Overview

* **Customer facing**: The Knowledge Articles widget provides a searchable list of knowledge articles on an Employee Portal page. It is useful on portal homepages, service pages, or knowledge-focused pages where users need quick access to published guidance.
* **Purpose**: Help users find relevant knowledge articles without leaving the page.
* **Default view**: The widget loads articles from selected knowledge bases and shows a small list with pagination.
* **Configuration**: Administrators can choose which knowledge bases and article types are searchable.

## What articles are shown

The widget searches published knowledge articles that the session user can access. Results are restricted to Employee Portal content and to the knowledge bases and article types selected in the widget configuration.

| Rule | Behavior |
| --- | --- |
| Portal visibility | The widget searches articles available for the Employee Portal. |
| Knowledge base selection | Only selected knowledge bases are searched. If the configuration is new, all available active Employee Portal knowledge bases are selected by default. |
| Article type selection | Only selected article types are searched. If no type is selected, all searchable article types can be included. |
| Access | Users only see articles they have access to through the configured knowledge and service visibility rules. |
| Paging | The widget loads articles in pages. The default page size is 5 articles. |

## User experience

* **Search**: Users can search knowledge articles using the search box. The search waits briefly while the user types, then refreshes the article list.
* **Knowledge base filter**: Users can filter the list by knowledge base. The dropdown includes an All option and one option for each knowledge base available to the widget.
* **Order options**: Users can order articles by published date, updated date, or most viewed. When HAi Search is enabled, the widget defaults to relevance search and the most viewed option is not shown.
* **Open article**: Users can open an article by selecting either the article reference or the article title.
* **Article feedback metrics**: The widget displays view, like, and dislike counts beside each article.
* **No results**: If no articles match the filters or search text, the widget shows a no results message.

## Administrator configuration

The configuration panel lets administrators control which knowledge bases and article types can be searched by the widget.

| Configuration area | Purpose | Recommended use |
| --- | --- | --- |
| Knowledge Bases | Selects which active Employee Portal knowledge bases are included in the widget search. | Select only the knowledge bases that are useful for the page where the widget is placed. |
| Knowledge Base Article Types | Selects which article types are included in the widget search. | Use article type selection when the page should focus on a particular type of knowledge, such as FAQs, guides, or policy articles. |

> **Recommendation:** Keep the widget focused. A smaller set of knowledge bases usually gives users more relevant results and makes filtering easier.

## Information shown in the widget

| Information | Shown as | Recommended use |
| --- | --- | --- |
| Article reference | A small link above the title. | Useful when users or support teams refer to article IDs. |
| Article title | The main clickable title. | The primary way users identify the article. |
| Knowledge base name | Displayed beside the title in italic text. | Useful when multiple knowledge bases are included. |
| Published date | Displayed on larger screens when available. | Helps users understand how recent the article is. |
| View count | Eye icon with a count. | Gives an indication of how often the article has been viewed. |
| Like count | Thumbs up icon with a count. | Shows positive feedback from users. |
| Dislike count | Thumbs down icon with a count. | Shows where articles may need improvement. |

## Responsive layout

The widget is designed to fit different portal page layouts and screen sizes.

* When the widget is placed in a narrow column, the search input is kept compact so the controls fit better.
* On wider layouts, the search box, knowledge base filter, and order control can sit on the same row.
* The article list stacks vertically, so users scroll down instead of sideways.
* The published date is hidden on smaller screens to keep article titles readable.
* Pagination is used so the widget does not become too tall when many articles are available.

## Localization and customization strings

The following strings are used by the widget or its configuration panel. Some strings are already translation keys, while others are currently rendered as widget text and can be considered for future localization if needed.

### Configuration strings

| Key or text | Default value |
| --- | --- |
| `employeePortal.widgets.knowledge.config.knowledgeBases.header` | Knowledge Bases |
| `employeePortal.widgets.knowledge.config.knowledgeBases.description` | Choose those that can be searched: |
| `employeePortal.widgets.knowledge.config.knowledgeBasesArticlesTypes.header` | Knowledge Base Article Types |
| `employeePortal.widgets.knowledge.config.knowledgeBasesArticlesTypes.description` | Choose those that can be searched (If no types are chosen, all will be searchable): |

### Widget display strings

| Text | Default value | Where it appears |
| --- | --- | --- |
| Search placeholder | Search... | Search input |
| Search aria label | Search knowledge articles | Search input accessibility label |
| Clear search aria label | Clear search | Search icon accessibility label |
| Knowledge base filter | Filter By Knowledge Bases | Knowledge base dropdown button |
| All knowledge bases | All | Knowledge base dropdown option |
| Order dropdown | Order By | Ordering dropdown button |
| Published date | Published Date | Ordering option |
| Updated date | Updated Date | Ordering option |
| Most viewed | Most Viewed | Ordering option when HAi Search is not enabled |
| Newest first | Newest first | Sort button title |
| Oldest first | Oldest first | Sort button title |
| Most viewed first | Most viewed first | Sort button title |
| Least viewed first | Least viewed first | Sort button title |
| No results | No results found | Empty state |
| Search results aria label | Search results | Results container accessibility label |

## Frequently asked questions

| Question | Answer |
| --- | --- |
| Can the widget search all knowledge bases? | It can search the knowledge bases selected in the widget configuration. For a new configuration, all available active Employee Portal knowledge bases are selected by default. |
| Can users filter by knowledge base themselves? | Yes. The runtime widget includes a knowledge base dropdown with an All option and individual knowledge base options. |
| What happens if no article type is selected? | The configuration description states that if no types are chosen, all article types will be searchable. |
| Why is Most Viewed sometimes missing? | When HAi Search is enabled, the widget defaults to relevance search and the Most Viewed sort option is not shown. |
| Does the widget show unpublished articles? | No. The operation is intended to return published knowledge articles that the session user can access. |
| Why does the article open in the self-service article page? | The widget links article IDs and titles to the Employee Portal knowledge article route and records the view source as self-service. |
