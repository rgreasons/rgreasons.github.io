---
title: Making QlikView Modern with Textboxes Everywhere
layout: post
tags: Qlikview
---

Although I started out my career in a traditional web developer role, I've gotten progressively closer to all things data-related.  Most recently, this has included a lot of development in business intelligence tools such as QlikView.  Qlikview is a powerful ETL and number-crunching tool but to call the look and feel of the application "dated" is putting it politely.  I have been able to develop QlikView applications that give the end users the impression of interacting with a website developed with modern HTML5/CSS3 by liberally using a simple QlikView object: the textbox.
<!--excerpt-->

Textboxes are powerful objects in QlikView because they combine a wide variety of visual style options while still being linkable to robust functionalities. The text area is like any other expression box so it can be used for calculations and KPIs. It can fire off actions to perform all sorts of behavior behind the scenes.  It has some of the most dynamic styling options of any object. Although I consider the textbox to be the ultimate jack-of-all-trades, I find that most uses fall into two categories: button replacement and page styling.

QlikView buttons look and feel ancient and can be replaced by textboxes to provide modern, flat designs. The default button style looks like it came straight off of a Netscape toolbar with the largest corner radius I've seen since 2002.  Even the less dramatic button styles still aren't truly "flat." It also provides fewer text formatting options, such as no text margin options. Everything a button does, a textbox does better.

Text boxes are also handy stylistic tools even when not displaying text or providing interaction. Div elements are to HTML what textboxes are to my QlikView apps: the building blocks of the overall design of a page. Whereas div elements act as HTML containers, think of textboxes as backgrounds- things to be layered *behind* the main content to provide the overall style.  Whereas an overall style can be provided by a well-designed background image, text boxes are a more dynamic option. Text boxes support transparency and conditional coloring and can be used as a dynamic background even if a sheet's layout is changed with shown/hidden objects. I also like to use text boxes as a way to visually group information; a text box behind a set of related sheet elements helps guide the user to the conclusion that the elements are related.

All of the use cases outlined above lead to the big flaw in using text boxes: object clutter.  All of the tips above are very impactful for the consumer of your QlikView app, but the developer is left weeding through all of the sheet's objects to make changes to the flow of the app. In order to mitigate some of these issues, it's important to give meaningful Object IDs and/or descriptions to your text boxes as you go along.  An Object ID of TX802 doesn't give any clues as to what the object does, but TXSheet2Group3Background can help a developer identify objects even after a long time away from the app. Regardless, this shouldn't be an issue - a good developer is *always* making sure to document as he goes along...

Using textbox objects in QlikView can help bring an outdated set of UI offerings into the 21st century with just a little bit of creativity and dilligent development practices. Even though it may not be the sexiest tool for the job, QlikView is still very capable of providing deep insights into data with just a little bit of elbow grease.
