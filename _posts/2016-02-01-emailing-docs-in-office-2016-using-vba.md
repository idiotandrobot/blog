---
layout: post
title: Emailing documents in Office 2016 using VBA
tags:
- Office
- Office 2016
- VBA
---
Historically the default 'Email' button in Word/Excel had some limitations that made it mostly unusable. 
It's tendency not to save messages to 'Sent Items' being it's worst fault, but also the default Subject and Body content weren't great.
To get around these limitations I'd been using a custom 'Email Document' button attached to an 'EmailDocument' macro.

**Original Macro:**

{% gist bfc1dbb11059836a9fce %}

After upgrading to Office 2016 this stopped working. For some reason it was no longer possible to explicitly declare object types 
so `Dim Outlook As Outlook.Application` and `Dim MailItem As Outlook.MailItem` would cause *Compile error: User-defined type not defined.* error messages.

Changing the declarations to `Dim Outlook As Object` and `Dim MailItem As Object` removed the error messages.

In addition `.Attachments.Add Source:=ActiveDocument.FullName, Type:=olByValue` no longer added the document as an attachment. 
It didn't error, it just didn't add the document.

Changing the call to `.Attachments.Add ActiveDocument.FullName` fixed the issue.

It's not clear why either of these things have become an issue in Office 2016, for me at least, but these were the changes required.
As an aside the 'Default' email behaviour and default content in Office 2016 seem much improved (saved to 'Sent Items', Subject is just filename).

**Modified Macro:**

{% gist 21fc665e652ffd53a81f %}
