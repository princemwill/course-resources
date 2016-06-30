# Library Teller - Bringing it together

## Overview
In this assignment we'll finish the work we started previously. By the end of this we'll have a simple library teller system that reads information from a file and outputs the due date for each media type

## Tasks

### Required Tasks

- [ ] Yak Shaving
  - [ ] Open a new issue called `03 -- Library Teller -- Your Name`, and copy/paste these tasks into the description
  - [ ] We'll use the same fork you created yesterday.
  - [ ] We'll create a new branch `Part3` by branching from what you worked on previously. Be sure you have the prior assignment done before starting this assignment. To create a new branch, make sure you're on the `master` branch and run `git checkout -b Part3`
  - [ ] Remember to continue to make frequent commits with descriptive messages


- [ ] Complete the `FileIO` class
  - [ ] Throw an appropriate exception when the file is not found
  - [ ] Open a StreamReader in the folder specified in the `path` variable that is passed into ReturnMediaFile
  - [ ] Implement a while loop to read the file line by line and add each line to mediaFile
  - [ ] Write a message to be written out when FileNotFoundException is thrown
  - [ ] Write a message to be written when a general exception is thrown


- [ ] Complete the `Program` class
  - [ ] Ignore this step: `//set the rental dates for each type via a static field`
  - [ ] Populate the `mediaToRent` object with the information from `Media.txt`
  - [ ] Use your RegEx in the second parameter of the `match` object. Be sure you have 3 capture groups. These will populate the type, title and length variables.
  - [ ] Create a Book object if `type` equals Book
     * Set the title variable for the new Book object
     * Set the length variable for the new Book object
     * Set the RentalLength variable for the new Book object
     * Add the Book to the rentedMedia list
  - [ ] Create a DVD object if `type` equals DVD
     * Set the title variable for the new DVD object
     * Set the length variable for the new DVD object
     * Set the RentalLength variable for the new DVD object
     * Add the DVD to the rentedMedia list
  - [ ] Create a Magazine object if `type` equals Magazine
     * Set the title variable for the new Magazine object
     * Set the length variable for the new Magazine object
     * Set the RentalLength variable for the new Magazine object
     * Add the Magazine to the rentedMedia list
 - [ ] In the foreach loop call `PrintMediaDetails()` to print out the details for each media item

### Stretch Tasks

- [ ] Implement UpdateMediaFile() in `FileIO.cs` to write the output of PrintMediaDetails() to a file in the same format

## Details
We'll be utilizing more object oriented programming features, file IO, and exception handling.

## Hints

Set a different RentalLenth period for each media type. When the program executes observe that they all function as intended.

All abstract properties or methods need to be overridden.

Virtual methods _can_ be overridden but you are not required to.

Once you have the code working for creating a Book object correctly you should be able to follow the same steps for the other two types.
