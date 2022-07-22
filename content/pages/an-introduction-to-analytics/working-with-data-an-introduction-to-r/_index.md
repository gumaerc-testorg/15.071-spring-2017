---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: 1 An Introduction to Analytics
parent_type: CourseSection
parent_uid: bebdc8ab-5b1f-9682-d6b7-62b671b5cf25
title: '1.3 Working with Data: An Introduction to R'
uid: 1ac933da-13d1-3dfa-2e38-03abf2d6971f
video_metadata:
  youtube_id: null
---
## Introduction to R

The slides for this sequence can be downloaded here: [Introduction to the R Programming Language (PDF)](./resolveuid/95e1dea61a0c566e8b1fe4ab6b1309ff).

Before beginning this lecture, please download and install R for free from the following webpage: [The R Project](http://www.cran.r-project.org).

At the top of the page, select your operating system (Linux, Windows, or Mac) and then follow the instructions. 

For most Windows users, you will select "install R for the first time" and then select "Download R 3.2.0 for Windows" at the top of the page. 

For Mac users, you will want to download R-3.2.0.pkg if you have OS X 10.9 (mavericks) or higher installed and R-3.1.3-snowleopard.pkg for earlier versions of the operating system.  Please note that either version of R will work for this course.

Once you have downloaded and installed R, please start the application, and then answer the following quick questions. This is to make sure that you have correctly installed R.

 

## Quick Questions for Installing R

When you start R, you should see a window titled "R Console". In this window, there is some text, and then at the bottom there should be a > symbol (greater than symbol), followed by a blinking cursor. At the cursor, type:

sd(c(5,8,12))

and then hit enter. You should see \[1\] followed by a number. What is this number?

Exercise 1

&nbsp;Numerical Response&nbsp;

 

Now type:

which.min(c(4,1,6))

at the cursor, and hit enter. You should again see \[1\], followed by a number. What is this number?

Exercise 2

&nbsp;Numerical Response&nbsp;

 

If you correctly answered both of these questions in R, you are ready to start the lecture! If not, please go to the discussion forum to get help installing R.

CheckShow Answer

## Important Note

If you downloaded and installed R in a location other than the United States, you might encounter some formatting issues later in this class due to language differences. To fix this, you will need to type in your R console:

Sys.setlocale("LC\_ALL", "C")

This will only change the locale for your current R session, so please make a note to run this command when you are working on any lectures or exercises that might depend on the English language (for example, the names for the days of the week).

- [BackVideo 6: This Class](./resolveuid/3697235ab9798298ffc243742c5e644d)
- [ContinueVideo 1: Why R?](./resolveuid/147b0a1bf22a4f9b0fd1d3a28f92f6da)