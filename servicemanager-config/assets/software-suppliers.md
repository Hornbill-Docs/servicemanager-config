# Software suppliers

The Software Suppliers page lists the vendors that are registered for use with the Software Asset Management. Typically, these vendors are automatically added as part of a discovery process, but you can also add suppliers manually.

Each vendor can have multiple software versions associated with it, which represent the different products offered by that vendor. This allows for better organization and management of software assets within the system. This is not designed to be a contact list for the suppliers, but rather a way to categorize and manage the software products that are being tracked.

![Software Suppliers Page](/_books/servicemanager-config/assets/images/software-suppliers.png)

## Adding a software supplier

The best way to add a software supplier is to use a discovery process, which automatically identifies and adds suppliers based on the software assets detected in your environment. The [Hornbill ITOM Discovery tool](/itom-user-guide/jobs/discovery-job) can help automate this process.

However, if you need to add a supplier manually, you can do so by following these steps:

1. Navigate to the Software Suppliers page in the Service Manager Configuration.
2. Click on the "Add Vendor" button.
3. Fill in the name and optionally provide an alias. The alias can be used for easier identification or to differentiate between suppliers with similar names.
4. Save the new supplier entry.

## Adding a product to a supplier

After a supplier has been added, you can associate products with that supplier. This is done by:

1. Selecting the supplier from the list.
2. Clicking on the "Add Product" button.
3. Entering the product name.
4. Saving the product entry.

## Adding a software version to a product

To add a software version to a product, follow these steps:

1. Select the product from the list of products associated with a supplier.
2. Click on the "Add Version" button.
3. Enter the version details, such as the version name or number
4. Save the version entry.

## Adding a supplier and product to a software asset

When you are managing software assets, you can associate them with the relevant supplier and product. This helps in tracking and managing the software assets effectively. To do this:

1. Navigate to the software [asset record](/servicemanager-user-guide/asset-management/asset-details) you want to associate with a supplier and product.
2. In the supplier field, select the appropriate supplier from the dropdown list.
3. In the product field, select the relevant product associated with that supplier.

![Associating a software asset with a supplier and product](/_books/servicemanager-config/images/software-asset-information.png)
