# Summer School MVC, part 2

## Overview

Polish up the Summer School MVC project to replicate all the functionality of the console version.

## Tasks

### Required Tasks

- [ ] Database
  - [ ] Clear up any issues with your database design
  - [ ] Update your model in Visual Studio
  - [ ] Re-export your `database.sql` file if you make any changes
- [ ] `Create`
  - [ ] Automatically calculate the enrollment fee based upon student name
  - [ ] Handle the special cases of Malfoy, Tom, Riddle, and Voldemort
- [ ] `Index`
  - [ ] Change the `Create new` link text to `Enroll`
  - [ ] Show/hide the `Enroll` link based upon the number of students
  - [ ] Include the total of all the enrollment fees

### Stretch Tasks

- [ ] Make the app look a little less like "stock" Bootstrap
- [ ] Extend the model to make the app more broadly useful
   - [ ] Allow for multiple `Courses`
   - [ ] Allow for multiple `Schools`
   - [ ] Keep track of how much students have paid

## Details

It's time to finish up your Summer School MVC app. Implement the logic from the Console version using the MVC framework.

Start by making sure your database includes everything you need it to include. Update your project if you make any changes.

Next, work in your views/controller to present relevant information. You should be able to use the existing views, but you may need to add some logic to your controller to have it:

- Automatically calculate the amount each student will owe
- Handle special cases
- Automatically hide/show the enrollment link when enrollment is full
- Calculate the total of all enrollment fees


### Stretch Tasks

As always, try to make the user experience better.

You can also extend the model to support multiple courses and/or multiple schools - create a new table to keep track of these, then add a foreign key to the `Students` table to link them. Then when viewing the Student enrollment, filter it based upon the selected course/school.

## Hints

If you have fields in your model that you want calculated in the controller, you need to make changes in a few places:
- The `ActionResult` method
  - `[Bind(Include = "param1,param2")]` parameter. Make sure that the only things listed in the `Include` string are the form fields you want the user filling out.
  - You need to **set** the fields inside the method before adding/saving it to the database. You may need to do this before checking if the `ModelState` is valid.
- The `cshtml` file for the view
  - Remove any reference to the fields that you are going to be calculating in the controller
