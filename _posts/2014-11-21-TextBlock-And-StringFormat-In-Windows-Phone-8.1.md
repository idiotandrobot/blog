---
layout: post
title: TextBlock StringFormat Support in Windows Phone 8.1 Projects
tags: [wp81 xaml]
redirect_from: /2014/11/21/TextBlock-And-StringFormat-In-Windows-Phone-8.1/
---
In trying to create a custom control for a Windows Phone 8.1 project I was having an odd problem where StringFormat didn't seem to be supported by the TextBlock control Text property any more so the following "Unsupported" style raised an error against *StringFormat=T*: 

{% gist dd6349cd134937012b39 %}

This was odd as the page was already covered in the "Supported" xaml shown above.

Which displayed (the integer values Minutes and Seconds) formatted to two digits as you'd expect.

A couple of [StackOverflow](http://stackoverflow.com/) questions seemed to confirm that StringFormat isn't supported (anymore):

- [StringFormat in XAML](http://stackoverflow.com/questions/24966425/stringformat-in-xaml)
- [Windows Phone 8.1 XAML StringFormat](http://stackoverflow.com/questions/24127262/windows-phone-8-1-xaml-stringformat)

And that the lack of support seems to be dependant on the type of project (i.e. WinRT doesn't support StringFormat so neither do Universal App projects).

Both of those questions have answers that suggest using a converter instead:

{% gist 101c1631fc96cf181c4f %}

This would also work but in the process of writing this post the original Clock style started working so I'm assuming something else I was doing in the custom control was at fault.

In summary StringFormat does seem to be supported still but if you get this error and need get it working quickly then either use an IValueConverter to get around the problem or write a blog post and that'll fix it.
