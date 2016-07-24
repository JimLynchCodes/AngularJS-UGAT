# AngularJS UGAT 

## "Ultimate Guidebook for Automated Testing"
 
### AngularJS 1.X Guide

Looking for Angular-UGAT, React-UGAT, or Java-UGAT?


Table of Contents
  - [Part 1: Intro to the UGAT](#Intro to the UGAT Series)
  - [History of the Testing Triplex](#history)
  - [Purpose of The Testing Triplex](#Purpose of The Testing Triplex)
  - [It's Not Specific To AngularJS](#It's Not Specific To Angular)
  - [This is a Guide for Developing Software](#This is a Guide)
  - [Is This Yet Another Interpretation of "Agile"?](#Is This Yet Another Interpretation of Agile?)
  - [Perfect Code Over Time Is Attainable](#Perfect Code Over Time Is Attainable)
  - No Amount of Testing Can prove no bugs from ISTQB, "Testing can shows the presence of defects: Testing can show that defects are present, but cannot prove that there are no defects". Since you could always be "missing one test" that *would* fail because of the bug in the system. If you can show that you have covered all situatinos with tests (a somewhat impossible goal) *and* all of those tests are passing then you can indeed be certain that that the software is absent of bugs. It's sort of a cop-out answer though, since the next question is, "well how do we know if we are missing certain tests?". Sometimes you can't foresee them, and you retrospectively write the tests to expose the bugs, but sometimes the missing or incorrect tests stem frmo not fully understand the requirements in the first place. 

Part 2: The Two Core Types of Automated Tests in AngularJS


Contributing to this README file.


<div name="Intro to the UGAT"></div>
## Part 1: Intro to the UGAT
---
<div name="history"></div>
### History of UGAT

UGAT (pronouced *ooh* like *"foo"* and *gat* like *"cat"*) is an acronym that stands for "Ultimate Guide (or Guidebook) for Automated Testing). I'm Jim Lynch, a web developer from New Jersey and organizsr of NG-NJ. While working on angularJS projects I was doing standard unit testing along with ui/web tests with Protractor. After really learning about BDD (Behavior Driven Development) I fell in love with the idea of putting your requirements into automated, execeutable tests. However, it was unclear how exactly to set up and practice BDD with an Angular, other SPA frameworks, or general JavaScript projects in a way that gelled nicely with the other automated tests. I've studying these different types of testing and tried them myself on real projects, I think I've discovered a way to develop software that works pretty well. This document attempts to distill this philosphy supporting and strengthening your codebase with automated tests and show you *how* to do it, specifically in the context of an AngularJS project.

<div name="Purpose of UGAT"></div>
### Purpose of UGAT

UGAT builds on the test-first theories of TDD (Test-Driven Development) and extends it by applying principles of BDD (Behavior-Driven Development). Thus, the testing triplex becomes a tao, or way of developing software where the result is truly transparent, agile, and just works. This guide provides a set of instructions for developing with The UGAT mindset, but it is up to you to find the tao on your own. You may or may not use the exact same tools as shown here, but hopefully you can take a way of thinking that will lead to successful testing implentations again and again.


<div name="Contributing to UGAT"></div>
### Contributing to UGAT

This software development philosophy is really only known about in a few small circles around New Jersey (that I know of, at least). We're always open to hearing feedback from others so don't be afraid to open an issue here, even if it's just a random question. If you feel something is missing from the Guidebook start a discussion by opening an issue, and if you want to write a section that's awesome too!


<div name="It's Not Specific To Angular"></div>
### It's Not Specific To Angular
It should be noted that the UGAT is not something that is dependant on the Angular library. It can be applied to really any project made from html, css, and javascript which can be tested with similar web/ui testing looks like Protractor (for other platforms Selenium does the same job and for mobile apps Appium is a good choice). Likewise, virtually every programming language has it's own unit testing framework (for JavaScript Jasmine or Chai-Mocha). An acceptance testing framework may be harder to find in obscure programming languages, but there's Cucumber for Rbuy, JavaScript, C++, Java, Python, Specflow for .NET, and support for many other languages. Searching "Cucumber for [X language]" will usually lead you to the choices for that particukar programming language. It's a little tricky because *"the best"* way is to have a *cucumberized* test runner for each seperately. A BDD version of unit tests and and BDD version of protractor tests. Although it's ideal, this may not always be available for yout platform or enviroment, but that's ok. Even if you can't "cucumberize" either set of tests, as  long as you have them you can use the BDD "given-when-then" steps when coding your tests and discussing examples of how the system is used.   


<div name="This is a Guide"></div>
### This is a Guide
This document is meant to be a guide for implementing automated testing in real life. Rather than be taken as gospel, the ideas expressed here are meant to convince you of the benefits of implementing these three types of automated testing. The prescribes methodoligies here have been tried a tested, but you are free to change things in your own case if you find it necessary to do so. This is a guide and may change over time and technologies change or others contrivute new ideas to it. 


 <div name="Is This Yet Another Interpretation of Agile?"></div>
### Is This Yet Another Interpretation of "Agile"?
This question here is whether Triplex Testing is really just another interpretation of "Agile methodologies". In some ways, yes. Triplex Testing values many of the core agile principles, but I like to think that Triplex Testing is a bit more description about *how* you acutally go about working this way from a programming point of view. In fact, Triplex Testing is so focused on the technical aspects that I would recommend any team attempting to try this to also look into [Design Driven Devlopment](#http://www.designdrivendevelopment.org/) and [Agile Project Management](#https://www.mountaingoatsoftware.com/agile/agile-project-management) since, while we think these are important, they are not covered in this guidebook. It seems that everyone has their own personal version of what agile means to them. We consider Triplex Testing to be a methodology that overlaps with Agile in that it values things like extreme programming, automated testing, continuous integration / deployment, plenty of communication among stakeholders, pair / mob programming, adaptive and interative cycles, and heavy customer / user involvement.

