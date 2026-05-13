---
layout: article-toc
---
# Relationships
The Service Manager Relationships allows you to define the different types of available relationships that can be used when linking different entities such as requests, services, assets, and more.

## Relationship Types
Relationship Types are defined terms that can be used for the creation of Relationship Links. When creating a Relationship Type consider the types of two way relationships that you would like to describe when linking two entities. As these will be used to create a relationship link, consider defining an opposite relationship type for each one created.

### Translations
Create Relationship Types in any additionally required languages.

Open an existing Relationship Type, and use the Add Translation button to choose the language you you wish to create the translation for, and then either use the Translate option to use Google's Translate service to suggest a translation of the relationship type, or enter the translation in the Relationship Type field.

### Edit
Change the display name of the Relationship Type by opening and editing the Relationship Type. Any changes will be inherited by any Relationship Links which are using the Relationship Type.

## Relationship Links
The Relationship Links lets you join or associate Relationship Types that will work together to describe the relationship between two entities.

### Add
1. Choose the + button to add a new Relationship Link
2. Choose the Feature which the new Relationship Link will be available for:
    * Request to Service - When linking additional Services to Requests
    * Request to Request - When linking Requests to Requests
    * All - Available for all Linking Features
3. Relationship - Choose one of the defined Relationship Types
4. Reverse - Choose another Relationship Type, which will be a direct reverse for the above Relationship

Examples
* Caused By > Causes
* Impacted > Impacted By
* Fixes > Fixed By

### Manage
* **Search**<br>Use the quick filter to search for specific Relationship Links
* **Filter**<br>Refine the displayed Relationship Links by All, Active or Deactivated
* **Active**<br>Mark a Relationship Link as deactivated, by sliding the Active toggle Off. This will prevent the Relationship Link from being available for selection in Service Manager
* **Delete**<br>If the Relationship Link has not been used in Service Manager, it can be deleted using the Trash Can icon

<!-- https://wiki.hornbill.com/index.php?title=Service_Manager_Relationships>
