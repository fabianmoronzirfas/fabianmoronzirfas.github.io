---
layout: post
title: "what is the InDesign targetengine ? "
date: 2011-11-13T15:26:00+01:00
tags:
- code
- javascript
- InDesign
tumblr_url: http://fabiantheblind.tumblr.com/post/12737564299/what-is-the-indesign-targetengine
---
if you want to store something e.g. a value or a string
 you can define a targetengine with a specific name of you choice
 this engine will exist until you close InDesign
 use this only if you know for shure what you are doing

for example run thisscript in InDesign:

#targetengine "session01"
var myValue = 0;
alert(myValue);
myValue++;


than this one;

#targetengine "session01"
alert(myValue);


InDesign will alert “0” at first as declared
 the second script will alert “1”

because “myValue” was stored by the targetengine “session1”
 and got incremented at the end of script one

with now targetengine declared InDesign will create at launch his own engine
 and destroy that after the script execution
 this is “garbage collection”
