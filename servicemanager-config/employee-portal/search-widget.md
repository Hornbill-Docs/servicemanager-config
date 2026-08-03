# Search Widget

The Search widget gives Employee Portal users a single search box for finding services, FAQs, service request catalog items, known issues, their own requests, and knowledge articles that they are allowed to access.

## Overview

The Search widget is designed for Employee Portal homepages and service pages where users need a quick way to find the right support content. The widget can search across several Service Manager content types and displays results in an autocomplete panel below the search box.

**Purpose**
Help users find relevant services, request forms, known issues, FAQs, knowledge articles, and their own requests.

**Access-aware results**
Search results are limited to content the session user can access through service subscriptions and portal visibility.

**Configurable presentation**
Administrators can set the title, description, placeholder text, service domain filter, and result types.

> **Customer summary:** Add this widget when users need a central place to search for service information and self-service actions from the Employee Portal.

## What users can find

The widget can return multiple result types. Administrators can leave all types available or restrict the widget to selected types.

| Result type | What it helps users find | Typical use |
| --- | --- | --- |
| Services | Services the user is subscribed to or allowed to access. | Help users navigate to the right service area. |
| FAQs | Published FAQs linked to accessible services. | Answer common questions without raising a request. |
| Service Requests | Catalog items and request forms available to the user. | Help users start the correct request process. |
| Known Issues | Published requests or known issues visible to the user. | Show existing issues before the user raises a new request. |
| My Requests | The signed-in user's own requests that match the search. | Help users find an existing request quickly. |
| Articles | Published knowledge base articles visible in Employee Portal. | Help users find knowledge content and guidance. |

> **Visibility:** The widget does not show all records in the system. Results depend on portal visibility, service subscriptions, configured return types, and the user session.

## User experience

![Search Widget](/_books/servicemanager-config/images/ep-search-widget.png)

**Search input**
Users type into a search field. Results are shown after the user enters more than one character.

**Autocomplete panel**
Results appear in a panel below the search input. The panel groups results by type when more than one type is searched.

**Type filters**
Users can switch between All, Service, FAQ, Service Request, Known Issues, My Requests, and Articles when those types are enabled.

**Result counts**
The panel shows result counts by category or a total count depending on the selected filter.

**More results**
When more results are available for the selected type, users can load additional results.

**Keyboard support**
Users can navigate the suggestion list using the keyboard and use Enter to select the active result.

### Example layout

**How can we help?**
Search for services, help articles, known issues, or request forms.

`Search for laptop support` 🔍

Filters: **All** | Service | FAQ | Service Request | Known Issues | My Requests | Articles

* **Laptop Support** — Service result for hardware and device support.
* **Request a replacement laptop** — Service Request result that opens a request form.
* **Known issue with laptop VPN connection** — Known Issue result with a Me Too action.

---

## Administrator configuration

Administrators can configure how the Search widget behaves on a portal page. These options affect what the widget searches and how the search box is presented.

| Configuration option | What it does | Recommended use |
| --- | --- | --- |
| Filter by Service Domain | Restricts searchable content to a selected service domain. | Use when the portal page is focused on a specific business area, such as HR or IT. |
| Filter by Types | Lets administrators choose which result types are searchable. | Use when a page should only search specific content, such as knowledge articles and FAQs. |
| Title | Adds a heading above the search box. | Use a short question or phrase, such as How can we help? |
| Placeholder | Sets the placeholder text inside the search input. | Use text that tells the user what they can search for. |
| Description | Adds supporting text below or near the search area. | Use for guidance, examples, or page-specific instructions. |
| Text Centered | Centers the title and description. | Use on homepage hero-style layouts where the search box is the main focus. |

### Filter by Types

When enabled, administrators can choose from these result types:

| Type | Description |
| --- | --- |
| Service | Search services that are available to the user. |
| FAQ | Search published FAQs visible to the user. |
| Service Request | Search catalog items that can be used to raise requests. |
| Known Issues | Search published issues that users can view and mark as affecting them. |
| My Requests | Search requests belonging to the signed-in user. |
| Articles | Search Employee Portal knowledge articles. |

> **Recommendation:** Keep the search scope focused. A homepage search can include all result types, while a service-specific page is usually easier to use when restricted to the most relevant types.

---

## Known Issues and Me Too

Known Issue results can include a **Me Too** action. When a user selects this action, the user is added as an impacted connection to the published issue. If the user clears the action, the impacted connection is removed.

**Why it helps users**
Users can confirm they are affected by an existing issue without creating a duplicate request.

**Why it helps support teams**
Support teams can see how many users are affected by a known issue and can use that context when prioritizing work.

---

## Responsive layout

The widget adjusts to the portal page layout and screen size.

* On wide layouts, the search input can be centered and displayed with a wider presentation.
* On smaller layouts, the input expands to the available width so users can search without horizontal scrolling.
* The results panel is repositioned when the page layout changes or the browser is resized.
* The autocomplete panel keeps the results scrollable when there are many matches.

---

## Localization and customization strings

The following keys are available for the widget configuration and search result interface.

### Configuration strings

| Key | Default value |
| --- | --- |
| `user.view.catalog-widgets.services.filter-service-domain` | Filter by Service Domain |
| `user.view.catalog-widgets.services.service-domain` | Service Domain |
| `user.view.catalog.widgets-config.services.filter-return-types` | Filter by Types |
| `user.view.catalog.widgets-config.services.return-types-service` | Service |
| `user.view.catalog.widgets-config.services.return-types-faq` | FAQ |
| `user.view.catalog.widgets-config.services.return-types-servicerequest` | Service Request |
| `user.view.catalog.widgets-config.services.return-types-knownissues` | Known Issues |
| `employeePortal.page.widget.search.requests` | My Requests |
| `user.view.catalog.widgets-config.services.return-types-articles` | Articles |
| `user.view.catalog-widgets.search.title` | Title |
| `user.view.catalog-widgets.search.placeholder` | Placeholder |
| `user.view.catalog-widgets.search.description` | Description |
| `user.view.catalog-widgets.search.text-centered` | Text Centered |

### Search interface strings

| Key | Default value |
| --- | --- |
| `employeePortal.page.widget.search.all` | All |
| `employeePortal.page.widget.search.service` | Service |
| `employeePortal.page.widget.search.faq` | FAQ |
| `employeePortal.page.widget.search.service-request` | Service Request |
| `employeePortal.page.widget.search.known-issues` | Known Issues |
| `employeePortal.page.widget.search.requests` | My Requests |
| `employeePortal.page.widget.search.knowledge` | Articles |
| `employeePortal.page.widget.search.load-more` | More Results... |
| `employeePortal.page.widget.search.me-too` | Me Too |
| `employeePortal.page.widget.search.result` | Result |
| `employeePortal.page.widget.search.results` | Results |
| `employeePortal.page.widget.search.more` | More... |
| `employeePortal.page.widget.search.less` | Less |
| `employeePortal.page.widget.search.no-results` | No results found |
| `employeePortal.page.widget.search.total` | Total |
| `employeePortal.page.widget.search.answer` | Answer |
| `employeePortal.page.widget.search.workaround` | Workaround |

---

## Customer notes

| Question | Answer |
| --- | --- |
| Why do I not see every service or request form? | The widget only returns content that is visible to the user and available through their service subscriptions or portal visibility rules. |
| What happens if no result types are selected? | When type filtering is not configured, the widget searches all supported types. When type filtering is enabled, selected types control the search scope. |
| Why does search not run after one character? | The autocomplete search begins after more than one character to reduce unnecessary queries and improve result quality. |
| What does Me Too do? | It marks the user as impacted by a known issue. Selecting it again can remove that impacted connection. |
| Can the widget text be tailored? | Yes. Administrators can configure the title, placeholder, description, and text alignment for each widget instance. |
