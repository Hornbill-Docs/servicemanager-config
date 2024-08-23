---
layout: article-toc
---
# Users
In Service Manager Setup, use the list of users in the main pane to manage who is using a subscription for Service Manager. You can add and remove users from this list to provide or take away access.

## Assigning users
Provided there are available subscriptions, click the **Assign User** button to allocate a subscription to a user.

Adding a user to the list reserves a subscription for that user.  Service Manager roles must be allocated to the users accounts before they can access the Service Manager app.

## Removing users
To remove a user from the list, select the check box next to the User ID and then click the **Remove User** button (the bin icon).

:::note
Removing a user from this list does not remove any assigned Service Manager roles or rights. The subscription may be automatically reassigned the next time the user logs in if the setting `subscription.application.allocateOnLogin` is set to `ON`.
:::

## Advanced

The following platform setting will automatically add a user to this list when they have been assigned a Service Manager role or right. 
|Setting|Description|Default|
|-|-|-|
|`subscription.application.allocateOnLogin`|When set to TRUE, a user who has been granted rights to an application will automatically be granted an application subscription when a free subscription for that application is available.|ON|