---
layout: post
title: Code by Charles Petzold
tags: [c#]
---
[Code](http://charlespetzold.com/code/index.html) by [Charles Petzold](http://charlespetzold.com/) is an excellent read, "a unique exploration into bits, bytes, and the inner workings of computers".

I thought it would be interesting to write an application to generate the combination of Braille, Morse and Binary found on the cover for any text input. 
I assumed someone would have done this already as the book is now a good 15 years old. 
If they have I couldn't find it. 


I did find this [Braille](https://code.msdn.microsoft.com/windowsdesktop/Drawing-Braille-Characters-920dbcea) project by Paul Ishak which seemed like a good starting point to get up and running quickly.
The intention was to switch to Wpf at some point but, as always seems to be the case with Wpf, getting from here to there doesn't seem worth the effort unless you really have to.
I'd be better off attempting it in javascript and html for a bit more universality.
In the meantime, [my WinForms attempt](https://github.com/idiotandrobot/petzold-code).

![Book Cover and Screenshot](https://raw.githubusercontent.com/idiotandrobot/petzold-code/master/README/Cover%20and%20Screenshot.png)
