# Variable Picker
The variable picker is available to use in most business process nodes and their fields, this includes:
* Human Tasks
* Custom Expressions following Decision nodes
* Integration Calls
* Automated Tasks
* Authorisations
The variable picker allows for the injecting or overwriting of variable values into node fields.

## Using the Variable Picker
It is possible to manually insert variables into node fields and this is covered in the Request Variables section, here we are focusing on the use of the variable picker.

The Variable picker can be opened in one of two ways:
* In most fields in business process nodes the Variable picker icon.png icon will be present and clicking on the icon will open the variable picker.
* Select ctrl or cmd and left mouse click, this will also open the variable picker if it is available and the Variable picker icon.png icon is not displayed

The variables which are available to use will be governed by which nodes precede the node you want to use the variable picker on in your business process, and therefore what information (variables) are available to you.

Available variables:
* **Global Inputs**<br>This option will contain any globally available variables such as requestid
* **Flowcodes**<br>This will list any variable data related to the entity in which the variable picker is being used. In order to have options presented here, the designer must use the relevant business process Get information nodes in the process stage prior to the node they want to make the variables available in.
Below is a list of the variable containers which can be used and their related Get Information node
    * Customer Details - Automated Tasks > Requests > Get Request Information > Customer Details
    * Organization Details - Automated Tasks > Requests > Get Request Information > Organization Details
    * Owner Details- Automated Tasks > Requests > Get Request Information > Owner Details
    * Request Details - Automated Tasks > Requests > Get Request Information > Request Details
    * Progressive Capture Answers - Automated Tasks > Requests > Get Request Information > Progressive Capture Answers
    * Service Details - Automated Tasks > Requests > Get Request Information > Service Details
    * Site Details- Get Request Information > Site Details
* **Tasks**<br>This will contain any tasks which precede the node into which you are looking to use the variable picker in the current stage of the business process.
Task variables which can be used include:
    * Outcomes
    * Completion Details
    * Completion Date
    * Owner
    * Custom Field Answers
* **Integrations**<br>This will contain any output parameter variables which are returned from any integration nodes which precede the node you are looking to use the variable picker in the current stage of the business process

## Inject or Overwrite
With the variable picker open and having navigated to the variable you wish to insert, you have two options to choose from:

* **Inject**<br>Clicking this option will add the variable to any other content which is currently in the node field (other variables, and or manual added content etc)
* **Overwrite**<br>Clicking this option will remove any existing content in the node field and replace it with the variable you have chosen.  

The variable picker allows for the adding of one variable at a time and the above process would need to be repeated where multiple variables are required to be added to the same node field, using the inject rather than overwrite option.

## Raw or Display Value
When choosing to inject or overwrite with a variable, it is possible to choose to use either the raw value or the display value of the variable. A good example of this is when you are configuring your progressive capture custom questions you may define a possible answer with both a value and a display value - these may be the same or they may differ. If you are creating different language versions of the question, you may want the raw value to remain the same but the display value may be different depending on the different language versions you have created, and as such you may choose to inject or overwrite with the display value rather than the raw value. The raw value will still be important elsewhere. You may make branching decisions in your process based on the raw value, as this value will always remain constant regardless of if the display value changes, this maybe the case depending on the users language settings or if you wish to edit how the display name is presented to the users in the future.