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
* **Capture Task Fields**<br>Enable custom fields on the task.
* ***Set Stage Checkpoints**<br>Optionally configure which stage checkpoints will be set on the completion of the task.

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