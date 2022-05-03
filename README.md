# Mini Project: Project Tracker

The task is to create a project tracker application using Bootstrap, jQuery, jQueryUI, Moment, and Google Fonts. 


### Task 1: HTML Build

1. A header/hero area is created to welcomes the users to the application and displays the current time and date using Moment.js with `setInterval()`.

2. A Bootstrap card component shows the instructions of how to use the app and a button to open a [Bootstrap modal dialog](https://getbootstrap.com/docs/4.5/components/modal/) (Ref).

3. The modal contain a form asking users to fill in the following data:

    * The name of the project

    * The type of project (use a `<select>` drop-down)

    * The hourly wage for the project

    * The due date for the project (use jQuery UI's datepicker with a minimum date setting in place)

4. A Bootstrap table is created to show the project's information can be printed to with columns for the following data:-

    * Project name

    * Project type

    * Hourly wage

    * Due date

    * Days until the due date (use Moment.js to calculate)

    * Estimated total earned (hourly wage at 8 hours per day multiplied by the number of days until the due date)


### Task 2 Capturing the Form Data

1. jQuery is used to set up functionality to capture the form's input elements on submit and use that data to create a new table row on the page.

2. Selecting and saving references to every DOM element to interact with to a variable (i.e., `var projectFormEl = $("#project-form");`) so that we can use these elements later.

3. A submit event listener is attached to the `<form>` element using jQuery.

4. On submission, four input values is captured from the form and pass them to another function to handle printing project data. Having one function that captures the data and another that prints the data to the page's `<table>` element will improve code readability.

---

### Task 3 Printing Project Data to Page

1. A function that is done to accept the four input fields' data as arguments.

2. A table row (`<tr>`) element is created and saved to a variable.

3. A table detail (`<td>`) element for each of the table columns created in Task 1.

4. For printing the days to the due date, Moment.js is used to calculate the difference between the due date and the current time in days. 

5. For printing the estimated total earned amount,  an eight-hour day is assumed for work. Multiply the hourly rate by 8 to get the daily rate, then multiply that value by how many days until the project is due to get the estimated total earned. 

6. Appended all `<td>` elements to the table row created, then append the entire row to the `<tbody>` element on the page.



### Task 4: Deleting Project From the Table

1. Update the table to accommodate one more column without a name.

2. When generating a new `<tr>` for a project, add one more `<td>` that holds a button for deleting a project from the list.

3. jQuery event delegation is used to attach an event listener to each of those buttons so that when clicked, the parent `<tr>` element will be removed from the page.

Technologies used:

HTML, Bootstrap and JQuery