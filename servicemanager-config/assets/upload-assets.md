# Upload Assets
You can manually upload multiple assets for specific asset classes from CSV files. This option is provided to allow the insertion of new assets into the Service Manager asset repository. Manual upload is generally used for static data. If you need to schedule the importing of new assets or updates to existing assets from discovery tools, MSSQL, or MySQL databases, you can find more information about the Asset Import utility in the [Data Imports Guide](/data-imports-guide/assets/overview).

As an Asset Management Administrator, select **Asset Upload** from the Asset Management icon in the application navigation bar.

## Creating the upload template
You can upload assets of different asset types, but only those that are managed under the same asset class, from a single CSV template. If you need to upload assets for types that are managed under different asset classes, you must create different CSV templates for each asset class grouping.

**To create your upload template:**
1. From the dropdown control against which you wish to import the new assets, select the asset class. This enables the option to download the related asset class template.
1. Select to download the template file.
1. Populate the template file rows and columns with the attributes for each asset you want to upload. Name and Type are mandatory attributes for each asset you wish to upload, regardless of its type or class.
1. Click **Save**.

While other attributes are not mandatory to perform the import, it is good practice to populate the attribute fields to match those that you enabled for each asset type (when you were defining the asset types).

For example, with *Used by* or *Site*, should you want the assets to appear as linked to these entities when performing other Service Manager actions (such as logging requests through Intelligent Capture and having the option to choose from a list of assets associated with the user), you should match up the attribute fields.

*Used by* requires the *usedById*, *usedByName*, and *usedByType* attributes to be completed. *usedByType* should be populated with either:
* 0 - if *Used By* is a coworker
* 1 - if *Used By* is a contact

*Owned By* requires both the *ownedById*, *ownedByName* and *ownedByType* attributes to be completed. *ownedByType* should be populated with either:
* 0 - if *Owned By* is a coworker
* 1 - if *Owned By* is a contact

Site requires both the *site* and the *siteId* attributes to be completed. *SiteId* refers to the database numerical value, not the display name.

Date attributes are required in the following format: yyyy-mm-dd hh:mm:ss

The `Country` field requires the ISO Alpha 2 codes as per the listing in [this Wikipedia article](https://en.wikipedia.org/wiki/ISO_3166-1).

The fields in the CSV file are mapped on the assets database table.

**To find which values and types need to be populated in the fields:**
1. Navigate to **Home > Applications > Service Manager > Entity Viewer**
1. Select **Database Schema Viewer** and navigate to the  `h_cmdb_assets` table.

## Validation
Against each asset class, you can configure which fields for that given asset class you wish to perform data validation. This is done before uploading the assets from the CSV file into the Service Manager asset repository.

As each customer may be using different unique identifiers, each customer can select from the available fields for each asset class, against which to perform the validation to ensure an asset does not already exist, and therefore avoid the creation of duplicate entries.
1. Click **Validation**.
1. Select one, multiple, or all of the available fields to perform the validation checks against.
1. Click **Save**.

Note that data validation, and the number of checks required, will extend the upload time for the asset import.

## Select CSV file to upload
To initiate the asset upload, select the CSV file you wish to use. Selecting the file initiates the import process.

On completion of the import, a report will be produced that  summarizes the following:

* The number of records processed
* The number of records successfully uploaded
* The records that failed to upload

If during the import process, specific rows of asset data are not able to be imported, this will be detailed below, including:

* Which rows failed
* The reason for the failures