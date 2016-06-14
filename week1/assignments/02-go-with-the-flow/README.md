# Go with the Flow

## Overview

Convert a flowchart into a console based program.

## Tasks

### Required Tasks

- [ ] Yak Shaving
  - [ ] Open a new issue in the `course-resources` repository called `02 -- Go with the Flow -- Your Name`, and copy/paste these tasks into the description
  - [ ] Create a new Console application project in Visual Studio called `GoWithTheFlow`, and make sure to check **Create a new Git repository**.
  - [ ] Create a remote repository on GitHub.com called `02-go-with-the-flow`
  - [ ] Set up your local repository to track with the remote repository
  - [ ] Make frequent commits with descriptive messages
- [ ] Gather Requirements
  - [ ] Find or create a flowchart that doesn't involve any loops
- [ ] Write Code
  - [ ] Translate the flowchart logic into code
- [ ] Submit
  - [ ] Fill out the homework submission Google form with a link to the issue and a link to your GitHub repository

### Stretch Tasks

- [ ] Translate a more complicated flowchart
- [ ] Use `goto` to handle flowcharts that repeat/loop
- [ ] Be flexible about input

## Details

In this assignment you'll be translating a flowchart into code. Flowcharts are visual representations of processes. Your code will involve converting the visual logic into the textual logic of C#.

First you'll need to find a flowchart that would be a good candidate for this assignment. A good candidate would involve several decisions, often involving "yes" or "no" answers to simple questions. You should avoid flowcharts that involve loops - that is, the flowchart shouldn't double back on itself, unless you are planning on tackling the stretch tasks.

Next you'll need to translate this into code. This will likely consist of `Console.WriteLine`, `Console.ReadLine`, and `if`/`else` blocks.

### Stretch Tasks

Find a more complicated flowchart. Figure out what would be necessary to translate it into code. If it involves loops or jumping around to different parts, you may want to look into using `goto` (though `goto` is generally [frowned upon](https://en.wikipedia.org/wiki/Considered_harmful), in this case it may be the best-suited tool at your disposal).

Another enhancement would be to make the program more forgiving. For example, allow the user to type "Yes", "yeah", "yep", or "definitely" in answer to a yes/no question.

## Hints

If you find yourself writing the same code over and over, then you may want to consider writing a static method to help you out with it. For example, if you want to be able to allow different phrasing for "yes/no" questions, you could write a helper static method that will take user input and return `true` or `false` for multiple inputs.

Here's an example of a very simplistic static method to accomplish this:

```cs
static bool GetChoice()
{
  var choice = Console.ReadLine();
  if (choice == "Yes")
  {
    return true;
  }
  else
  {
    return false;
  }
}
```

To use this method, just treat the result as a `bool`, which can be used directly with an `if`. Here's an example of what this might look like inside your `Main` method:

```cs
Console.WriteLine("Is today a Tuesday?");
if (GetChoice())
{
  // they typed "Yes"
  Console.WriteLine("Wear galoshes!");
}
else
{
  // they didn't type "Yes"
  Console.WriteLine("Don't wear galoshes!");
}
```
