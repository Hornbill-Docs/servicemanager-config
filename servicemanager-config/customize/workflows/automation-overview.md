# Overview
A Hornbill Automation is a definable automated task that will occur within the workflow. The available Hornbill Automations are provided by each application that uses Workflows.

## Adding a Hornbill Automation
When viewing a workflow canvas, there are a couple of ways to add a Hornbill Automation.

* **Add after existing node**<br>Drag an arrow from an existing workflow node. When you let go of the mouse button, you are presented with a list of nodes that you can select from. Select Hornbill Automation

* **Add between existing nodes**<br>Click on an arrow between two existing nodes. Once the arrow is selected, right-click on the arrow and select Add node between connected nodes. Select Hornbill Automation from the list of available nodes.

Hornbill Automations can be easily identified in a workflow as a light blue rectangular node.

## Properties
The properties of a Hornbill Automation can be accessed by either hovering the mouse pointer over the node and then clicking on the cog icon or you can simply double-click on the node.

* **Language**<br>This will default to the language of the user that is adding the node. After the node has been added, you may consider adding translations for other languages by selecting a language from this list.
* **Display**<br>This is the name of the node that will be displayed in the node when viewing the workflow. This is also displayed when using the variable picker. The display should easily identify the node and its purpose.

### Process
* **Help**. Each Hornbill Automation includes help information that is accessible from the Process section.
![Access Process Help](/_books/servicemanager-config/customize/workflows/images/automation-help.png)

    This help information includes valuable information about the inputs and outputs of each Hornbill Automation. The help information displayed will be in context with the selected Task.
    ![Process Help](/_books/servicemanager-config/customize/workflows/images/automation-help-popup.png)


* **Application**<br>Each application can provide a set of Hornbill Automations to select from. A workflow that is executed in one app can perform an automation in another app. This option allows you to browse and select from the applications that provide automations. This node will run under the context of the selected application.

* **Scope**<br>The scope can either be set to Entity or Application.
    * ***Application***<br>When selected, the Type field shows a number of different categories of automation that are not directly related to an application entity. This list is independent of the selected application and will be the same for all selected applications.
    * ***Entity***<br>Enables the entity option where you can select from a list of entities that relate to the selected application.
* **Entity**<br>This option is only available when the Scope is set to Entity. This list will include entities associated with the selected application that have at least one automation available.

    :::tip
    An entity is an identifiable object defined within each application. Hornbill Automations are designed to update the attributes of these objects.
    :::

* **Type**<br>Tasks are categorized into types. Selecting a Type will make the related tasks available in the Task field.
* **Task**<br>This is the definable automation where you can specify inputs that are needed for the automation to run.
* **Result Reference**<br>When there is more than one Hornbill Automation node that performs the same task, unique references can be used to access the outcomes of each node at the time that they were run.

## Options
The list of options provides inputs that are used to perform the task. These options will vary with each task.

* **Mandatory**<br>Options that are mandatory display a vertical red bar on the left-hand side.
* **Information**<br>Each option has an information icon where you can read some basic information about that option. Additional information can be found in the help by clicking on the ? icon.
* **Auto/Manual/Variable/Ignore**<br>Each option allows you to select how it will be populated.
    * ***Auto***<br>This will use a default value for the option. Not all options have a default value and you will have to refer to the documentation for each individual automation to confirm if this can be used.
    * ***Manual***<br>Use this to manually type in the text or select from a drop-down box if provided.
    * ***Variable***<br>Use this to allow for the use of a variable that can be selected using the Variable Picker.
    * ***Ignore***<br>This is only available when an option is not mandatory. This ensures that no value is used with this option when the automation is run. Non-mandatory options will default to Ignore.

## Set Stage Checkpoints
You can select one or more checkpoints to be set when this node is reached.

## Output Params / Context Reference
Hornbill Automation nodes provide output parameters which can be accessed through Variable Picker or Decision node in a Business Process. The value in Result Reference of a node is appended to the reference of each output parameter.