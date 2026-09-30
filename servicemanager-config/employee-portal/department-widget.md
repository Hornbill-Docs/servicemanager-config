# Department Widget

The Department widget is part of the [People Hub for NHS Trusts](https://www.hornbill.com/solutions/nhs-hrsm/) solution and is available to registered users

The Department widget gives a budget holder or finance manager a view of their department's funded positions, how much of each one is filled, and which employees occupy them.

## What the widget shows

![Department widget example](/_books/servicemanager-config/employee-portal/images/department-widget.png)

* What positions does my department have, and what are they funded at?
* How much of each position is actually filled, and how much is vacant?
* Who is in each position, and on what basis?

## Who can see it

The widget only ever shows a person the departments they are responsible for. It works this out automatically, with no separate permission list to maintain.

Each department record holds up to six responsible people: four budget holders, a finance manager and a senior finance manager. Each of those is recorded as an assignment reference. When someone opens the widget, it looks up the assignments belonging to them and shows every department where one of those assignments appears in any of those six roles.

* If you hold no budget and are not a finance manager, the widget shows you nothing.
* If you are responsible for three departments, you can switch between those three.
* When responsibility changes in the source system, the widget follows automatically at the next refresh.

Both full user accounts and basic accounts can use the widget, so it is suitable for managers who do not have a Service Manager license.

## Choosing a department

The department selector sits at the top right of the widget. It opens with the first of your departments already selected.

* Select the button to see the full list of departments you are responsible for.
* The list has its own search box, useful if you cover many departments. Type any part of a department name to narrow the list, then choose one.
* A department that is recorded against several cost centers still appears only once.

> **Note:** Changing department resets the view back to the first page and clears any search you had running, so you always start from a clean list.

## The two views

A second button at the top switches between two ways of looking at the same department.

|View|One row per|Best for|
|---|---|---|
|Show Positions|Position|Seeing the shape of the department, what is funded and what is vacant|
|Show Assignments|Person in a position|Seeing everyone in the department at once, and finding a particular person|

## Searching

The search box at the top left searches whichever view you are currently in. Partial matches work throughout, so you never need to type a whole value.

|In this view|Search matches|
|---|---|
|Show Positions|Position title and position number|
|Show Assignments|Employee name, employee number, assignment number, position number, and position title.|

Because position number matching is partial, position 123456 can be found by searching 123, 456 or 234. The same applies to employee and assignment numbers in the Assignments view.

> **Note:** The department selector has its own separate search, which filters the list of departments rather than the table.

## Where the information comes from?

Everything the widget shows comes from your organization's staff records, which are kept up to date from your HR system. The widget itself holds no separate copy and nothing in it can be edited.

Three kinds of record sit behind it:

* **Departments**: Records the cost center and who is responsible for the budget.
* **Positions**: Records the job, its grade, its subjective code and how much it is funded for.
* **Assignments**: each recording one person in one position, with their FTE, category and status.

Because of that, anything that looks wrong in the widget is almost always a reflection of the source record rather than the widget itself. If an employee appears in the wrong department, or a position shows an unexpected funded figure, the correction belongs in the source system and the widget will follow at the next update.
