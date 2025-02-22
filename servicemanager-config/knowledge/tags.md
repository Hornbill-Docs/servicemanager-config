# Knowledge tags
Tags can be used to help search for knowledge, identify trends, and identify areas that might be lacking in information. Navigate to Configuration > Service Manager > Knowledge to create tags and manage the tags within your tag cloud. 

To pre-define tags within Configuration, you must have either the Knowledge Administrator role, or a custom role with the `canAdministerKnowledge` application right. All Knowledge managers and contributors can then select from existing tags to attach to their articles.

:::tip
Knowledge base admins, owners, and contributors can add new tags directly within an article.  Service Manager Admins can disable this by changing the app setting `knowledgeArticle.form.tags.addNew` to OFF. This will apply to all knowledge bases. This can be used when great control over the available tags is required.
:::  

## Cloud view
The Cloud View is the default view when entering the tags. This is where you add new tags.

![Tag Cloud](/_books/servicemanager-config/images/tag-cloud.png)

### Adding a new tag
In the text field beside the **Add Tag** button, type the name of the tag that you wish to add and click **Add Tag**. The new tag is then visible in the tag cloud.  

The size of the text in the cloud tag represents how often the tag.  The larger the text, the more the tag has been used.

## List view
From the Cloud view, click the **List View** button to access the List view. Here you can manage all existing tags.

![Tag List](/_books/servicemanager-config/images/tag-list.png)

To modify a tag, click the edit icon within its row. You can:
* Change the name of the tag.
* Add a new translation for the tag.
* Delete a tag.

Next to each tag's name in the list, a number shows how many times the tag has been used in articles.

