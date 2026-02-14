# Request Variables

As a process designer it is beneficial to have access to and use variables in your process nodes for varying purposes, it could be to insert answers from Intelligent Capture questions into the summary, description or custom fields of a request, to branch and make decisions in your process based on the site of the request customer, or the outcome to particular tasks. You may even want to add details into a task or authorization details field which is made up of details from the parent request, Intelligent Capture answers or related entities (Customer, Service, Organization etc), or you may simple want to assign tasks and authorizations to variables such as a requestors owner.

In all these examples and many more there is a need in the designer to be able to insert these variables into the relevant fields on the different business process forms

## Using Variables

It is possible to both manually add variables to node fields and also use the Variable Picker to inject variable values into node fields. Please follow the link in the related articles section to learn more about using the variable picker.

When working with variables it is important to understand what you can use, when and how.

In many business process node fields there will be the option to use variables, the nodes include:

* Human Tasks
* Custom Expressions following Decision nodes
* Integration Calls
* Automated Tasks
* Authorizations

The key consideration when looking to add variables into a field, or use a variable to make a decision in the process node, is do I have the variable information available to me, preceding the node I want to use it in? By this I mean have I used the Automated Task > Requests > Get Request Information nodes to load the required variables into my process, this could be:

* Request Details
* Customer Details
* Organization Details
* Intelligent Capture Answers (please note: this is limited to the first 200 question & answer combinations)

Or is the node preceded by a task off which I want to branch from or another integration call node with output values.

If you have included the relevant nodes before a node in which you want to use a variable then you can then either use the Variable Picker or in some cases manually add the variable in a field.

Once you have added the variables to the node fields they will display like: &[global["flowcode"]["summary"]]

Once the request runs and the variables are added to displayed request fields, task descriptions etc they will appear as shown in the image opposite

## Variables in Custom Expressions

In the same way as injecting variable values into node fields, you may also want to use variables to help with decisions and branching in your processes.

Here the same rules apply and you would need to ensure you have the relevant nodes preceding any decision node off which you wanted to evaluate variables to branch your process flow.

On the lines out from a decision node, you can use the Custom Expression option and then use the Variable Picker to select which variable you want to evaluate and either use a static or variable for the answer you are looking for to folow that path in your flow.

## Manually Adding Variables

Hornbill have provided the Variable Picker to make the adding of variables easier, however if you wanted to manually add variables then the below will provide the format which can be used.

* Request Details Variable: &[global["flowcode"]["summary"]] or &[global["flowcode"]["customFieldA"]]
* Service Details Variable: &[global["flowcode"]["serviceName"]] or &[global["flowcode"]["customA"]]
* Customer Details Variable: &[global["flowcode"]["jobTitle"]] or &[global["flowcode"]["custom1"]]
* Organization Details Variable &[global["flowcode"]["industry"]] or &[global["flowcode"]["custom2"]]

Request variables are fairly self explanatory, and a list is provided below. Answer variables are specific to the Custom Form defined in the Get Request Information > Intelligent Capture Answers node specified before the node you wish to use them in, and can be included simply by referencing them as follows:

* &[functions.pcf("Application_Access","field_2")] - Where in this case Application_Access is the custom form name and field_2 is the specific question name on the custom form (if you have renamed the default field names on the custom from from field_2 for example to anything else, then you would need to use the new field name here.)

### List of Available Request Details Variables

&[global["flowcode"]["assignedTeam"]]<br>
&[global["flowcode"]["authorisation"]]<br>
&[global["flowcode"]["closureCategory"]]<br>
&[global["flowcode"]["customer"]]<br>
&[global["flowcode"]["customerCompany"]]<br>
&[global["flowcode"]["customerManager"]]<br>
&[global["flowcode"]["customerPrimaryEmail"]]<br>
&[global["flowcode"]["customerPrimaryPhone"]]<br>
&[global["flowcode"]["customerSecondaryEmail"]]<br>
&[global["flowcode"]["customerSecondaryPhone"]]<br>
&[global["flowcode"]["dateLogged"]]<br>
&[global["flowcode"]["description"]]<br>
&[global["flowcode"]["impact"]]<br>
&[global["flowcode"]["loggingCategory"]]<br>
&[global["flowcode"]["owner"]]<br>
&[global["flowcode"]["ownerId"]]<br>
&[global["flowcode"]["priority"]]<br>
&[global["flowcode"]["requestId"]]<br>
&[global["flowcode"]["resolution"]]<br>
&[global["flowcode"]["service"]]<br>
&[global["flowcode"]["source"]]<br>
&[global["flowcode"]["site"]]<br>
&[global["flowcode"]["status"]]<br>
&[global["flowcode"]["summary"]]<br>
&[global["flowcode"]["timeLogged"]]<br>
&[global["flowcode"]["urgency"]]<br>
&[global["flowcode"]["withinFixTime"]]<br>
&[global["flowcode"]["withinResponseTime"]]<br>
Plus custom fields in the format : &[global["flowcode"]["customFieldA"]]
