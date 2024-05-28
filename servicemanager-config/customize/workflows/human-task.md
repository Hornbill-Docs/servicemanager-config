# Human Task
When creating a human task it is possible to define this in one or multiple languages, by default this will be English, however it is possible to create copies of the human task in any other languages enabled on your instance. This is a consideration where those who maybe assigned tasks are working in different languages, and they will receive the human task either in the default language or in the language defined in their profile if the human task is configured in the different languages.

## Options
* **Display**<br>This is simply the display name for the human task node in the business process designer, it will not appear on the human task.
* **Title**<br>This will appear as the title of the human task.
* **Category**<br>Set a category that will appear on the human task.
* **Priority**<br>Set a priority to indicate the priority of the task.
* **Owner**<br>The Owner is an important consideration, as they can be notified about the task in reminders, and will also have the ability to reassign the assignee if required. The Owner can be either a named user or a variable.
* **User**<br>Pick from a list of co-workers.
* **Variable**<br>In order to see a list of possible variables like request owner, you will need to precede the human task node with the Automated Task Node > Request Entity > Get Information > Request Details.
* **Assign To**<br>Choose who the human task will be assigned to, this can be a named user, group, role, or variable.
    * ***User***<br>Pick from a list of co-workers.
    * ***Variable***<br>In order to see a list of possible variables like request owner, you will need to precede the human task node with the Automated Task Node > Request Entity > Get Information > Request Details or any other node that outputs a user ID as a value.
    * ***Role***<br>This will be populated from the default roles and any custom roles defined on your instance. Any Users who are assigned the role will receive the human task, any notifications and will have the ability to complete the human task.
    * ***Group***<br>This will be populated from the defined groups on your instance. Any Users who are members of the group will receive the human task, any notifications and will have the ability to complete the human task.
* **Lifespan Settings**<br>It is possible to set a start date, due date and expiry date for the task based on either a predefined value, or based on a variable like respond by or fix by from the parent request.
    * ***Start After***<br>Set this to either X Days, X Hours and or X minutes after the creation of the Task, or base this on a variable like log date, resolve by, or fix by. If using the Variable option remember to precede the node with the Automated Task Node > Request Entity > Get Information > Request Details.
    * ***Due After***Set this to either X Days, X Hours and or X minutes after the creation of the Task, or base this on a variable like log date, respond by, or fix by. If using the Variable option remember to precede the node with the Automated Task Node > Request Entity > Get Information > Request Details.
    * ***Expires After***<br>Expires is a valid outcome for a human task, and setting a value here will allow you to via a decision node following the task allow for branching based on an outcome not being selected but the task expiring. Set this to either X Days, X Hours and or X minutes after the creation of the Task, or base this on a variable like log date, respond by, or fix by. If using the Variable option remember to precede the node with the Automated Task Node > Request Entity > Get Information > Request Details.

    :::tip
    When using variables for the Lifespan Settings these must be in the ISO Date/Time format, e.g. 2021-11-26T11:30:00.000Z.     Values from a Date/Time picker will be in this format, but values from a Date Picker will not.
    :::

* **Task Details**<br>Define the details for the human task, this can be a combination of text and if required variables from the parent request which the task is related too, this could be the summary or description fields, custom fields, or even answers to progressive capture questions - see more about inserting request variables here.
* **Task Options**<br>
    * Hide the completion Reason when completing the task - decide if the reason field is not required when completing the task via an outcome.
    * Do not allow completion of the task unless it is 100% complete - this option becomes available if Checklists have been enabled on the task, and you do not want to allow the task to be completed whilst there are outstanding checklist items.
    * Decide if you want to display the Time Spent option to the user who is completing the human task
* **Outcomes**<br>Configure what possible options the user completing the human task can choose from when completing the human task. By default two are provided, Completed and Not Completed.
* ***Set Stage Checkpoints**<br>Optionally configure which stage checkpoints will be set on the completion of the task.

## Capture Task Fields
### Configuring Capture Task Fields

* **Field Properties**<br>Provide a title for the field, add a custom field id or leave as standard and add placeholder text if needed.
* **Default Flags**<br>Configure if the field is mandatory, visible on the form, in read only view etc.
* **Field Type Settings**<br>Configure the type of capture you wish to use - single, multi-line, static or dynamic drop down, check box, radio box, label etc and provide the context based attributes as required.

Click Apply Settings to add the capture field to the task

* Use the Language option to define different language versions of the capture field, which will be displayed to a user based on the language set in their profile.
* Repeat the process for any additional capture fields which are required for the task.

### Considerations
* **Default Reason field**<br>You may decide that the Reason field on the task is no longer relevant if you have added your own capture fields, and this can be hidden from the task by ticking the Hide reason option under the Task Options settings.
* **Setting Capture Fields Per Outcome**<br>It is possible to configure capture fields which are tied to the selection of an outcome on a task, and will only be presented and visible once a specific outcome has been chosen. This is covered in detail in the Outcomes wiki page.

:::tip
Information It is possible to use both task capture fields and outcome capture fields on the same task, but you are advised to check and ensure that none of the capture fields are using the same field id.
:::

### Using the Answers to Capture Task Fields
Once a task has been completed and any capture task fields completed, the answers from these fields are available to be used elsewhere in the lifecycle of the business process.

* Branch and make decisions on the answers using the custom expression builder and selecting the relevant task and capture field to evaluate.
* Inject the answers from capture task fields into request fields, or other tasks using the variable picker following the task but in the same stage of the process.
* The task and capture field answers will be written to the timeline of the entity the task has been completed against.

## Checklists
Add To Do checklists to a task

Click on Manage Checklists on a task and Add Group
1. Give the Checklist Group a Name
1. Click on the + button to add your first and subsequent checklist items
1. Use the arrows to re-order the checklist items in the checklist group
1. Use the trashcan to remove checklist items and or the checklist group
1. Use the Add Group to add subsequent checklist groups to the same task
1. Use the arrows to re-order the checklist groups on the task
1. Click Apply to add the checklist group/s to the task

### Managing Checklists
Click on Manage Checklists to edit or delete the checklists associated to the task.

### Considerations
When a user ticks a checklist item as having been complete on the task, the % progression through the checklist items will be indicated on the task.

If you wish to prevent the completion of the task while there are any outstanding checklist items on the task, select the Do not allow completion unless it is 100% complete within the Task Details section when configuring the task.

<!-- https://wiki.hornbill.com/index.php?title=BPM_Human_Tasks-->
<!-- https://wiki.hornbill.com/index.php?title=Checklists -->
<!-- https://wiki.hornbill.com/index.php?title=Capture_Task_Fields -->