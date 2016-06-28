# Express Yourself

## Overview

Write some regular expressions to find important bits of information.

## Tasks

### Required Tasks

- [ ] Yak Shaving
  - [ ] Fork and clone the [express-yourself](https://github.com/wcci-summer-2016/express-yourself) repository
  - [ ] Make frequent commits with descriptive messages
- [ ] Systems Check
  - [ ] Uncomment the first test and verify it runs (and fails)
- [ ] Write `Parser` methods to pass tests
  - [ ] `GetTitle`
  - [ ] `GetType`
  - [ ] `GetLength`
  - [ ] `IsValidLine`


### Stretch Tasks

- [ ] Create Extra Classes
  - [ ] Create an `Item` class
  - [ ] Create `Book`, `DVD`, and `Magazine` subclasses of `Item`
- [ ] Write Additional Methods
  - [ ] Write `GetBook`, `GetDVD`, and `GetMagazine` methods
  - [ ] Write tests for the above
- [ ] More Better-er
  - [ ] Decide on some extra functionality that could be useful with parsing a text file like `Media.txt`, write tests for it, and implement it

## Details

Yet again you find yourself in the junior dev position where someone has written a bunch of tests, and you need to write code to pass those tests. In this instance, you're working on an application that will store information for library catalogs. You don't know all the details, and you don't really have to at this point.

The QA programmer wrote the tests using [NUnit](http://www.nunit.org/). This time, he commented all of them out, so you can uncomment them as you make them pass and can more easily see what's passing/failing.

Look in the `ExpressYourselfTests.cs` file inside the `ExpressYourselfTests` project, and uncomment the `TestCase` lines to activate them. I suggest you do them one at a time (or perhaps a group of them relating to one method at a time).

To run the tests, you can click the **Start** button in Visual Studio.

It's possible that, as you are attempting to make some tests pass, others may fail that once passed. This is okay! Just focus on making one test pass at a time. If a test stops passing, then you can revisit it later.

I also encourage you to make a new commit after causing each new test to pass. You can use Git to look at the differences between a version with passing tests and a version with failing tests, and that can sometimes help isolate issues.

### Stretch Tasks

Rather than just focusing on the individual pieces of a media item, it would be helpful to think of them in a more object-oriented way. You can imagine that `Book`, `DVD`, and `Magazine` would be subclasses of an `Item` class.

Write the above classes and write methods that will take a `string` and return a `Book`, `DVD`, or `Magazine` object.

Writing tests for this might be a little trickier than what you're used to, but give it a shot!

## Hints

You may want to install the [NUnit 3 Test Adapter](https://github.com/nunit/docs/wiki/Visual-Studio-Test-Adapter) for Visual Studio.

Install it from the `Tools > Extensions and Updates` menu item and restart Visual Studio.

Then show the **Test Explorer** window by clicking `Test > Windows > Test Explorer`, and click the **Run All** button to actually run the tests.

This is not necessary for running tests, and it can take a little bit longer to run tests, but some developers prefer the visualization of each passing/failing test right inside Visual Studio.
