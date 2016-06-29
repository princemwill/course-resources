# Library Teller - Building the Objects

## Overview
The next couple assignments will have you working on a library teller system. As we work on more of the components we'll be working towards a more complete system.

## Tasks

### Required Tasks

- [ ] Yak Shaving
  - [ ] Open a new issue called `02 -- Library Teller -- Your Name`, and copy/paste these tasks into the description
  - [ ] Fork and clone the [library-teller](https://github.com/wcci-summer-2016/library-teller) repository
  - [ ] Make frequent commits with descriptive messages
  - [ ] Feel free to use [Regexr](http://regexr.com/) to help with designing the Regular Expression. If you copy and paste the contents of Media.txt into http://regexr.com you are able to obverse the match results as you design your Regular Expression.


  *Given the following CSV format:*  
  `Type: Book,Title: The Count of Monte Cristo,Length: 928 pages`

- [ ] Write a [Regular Expression](https://en.wikipedia.org/wiki/Regular_expression) that meets the following criteria
  - [ ] Starts by matching the beginning of a line
  - [ ] Matches everything after `Type:` but before the first comma and stores the value in capture group 1
  - [ ] Matches everything after `Title:` but before the second `,`(comma) and stores the value in capture group 2
  - [ ] Matches everything after `Length:` and stores the value in capture group 3
  - [ ] Ends by matching the end of the line
  - [ ] Accounts for whitespace after the `:`(colons) but before the capture group start

  Feel free to reference Media.txt to view the format of the document. This is the file we'll be processing in the next assignment.

  ---

- [ ] Write a `DVD`, `Magazine`, and `Book` class that
  - [ ] Inherit from the `Media` class
  - [ ] Print media details() should print:
     * The Type followed by the title
     * The length
     * The rented date
     * The return date() rented date


### Stretch Tasks

- [ ] RegEx accounts for errant spaces throughout the string
- [ ] RegEx accounts for any arbitrary non word character delimiter
- [ ] RegEx matches the digit data in the length field without any string data(number of pages/length/running time/etc)
- [ ] Make RegEx the matching for `Type:`, `Title:` and `Length:` all case insensitive

### Stretch Armstrong Tasks

- [ ] Only match `Book`, `DVD` and `Magazine` as valid `Type:` values. Reject all other values

## Details
Regular expressions can be used to match certain elements of a string. These can be separated out with capture groups and returned separately. This allows us to pull out specific elements and manipulate them separately.

## Hints

Start by building your regular expression in order. Slowly build up the expression while working forward.

If you are having trouble with your regular expression , try modifying the string so you can focus on just matching the first part. Once you have that completed, continue by adding on the next section to match.

If you are unsure on how to use a `DateTime` type look at a few examples online such as [http://www.dotnetperls.com/]

With the `DateTime` can you utilize methods like .AddDays(days) to easily modify the date.

In your derived classes you may need to utilize the `new` and `override` keywords when overriding methods and fields
