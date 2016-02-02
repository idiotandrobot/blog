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
After upgrading to Office 2016 this stopped working.

**[Original Macro](https://gist.github.com/idiotandrobot/bfc1dbb11059836a9fce):**

{% gist bfc1dbb11059836a9fce %}

For some reason it was no longer possible to explicitly declare object types 
so `Dim Outlook As Outlook.Application` and `Dim MailItem As Outlook.MailItem` would cause *"Compile error: User-defined type not defined."* error messages.

Changing the declarations to `Dim Outlook As Object` and `Dim MailItem As Object` removed the error messages.

In addition `.Attachments.Add Source:=ActiveDocument.FullName, Type:=olByValue` no longer added the document as an attachment. 
~~It didn't error, it just didn't add the document.~~
On commenting out `On Error Resume Next` an "*Object doesn't support named arguments.*" error is raised.

Changing the call to just `.Attachments.Add ActiveDocument.FullName` fixes the error.

**NB:** Prior to finding these errors I hadn't tried this macro on a document stored in OneDrive. Because the `FullName` for a OneDrive document is it's web rather than local path, Office to attempts to redownload the document leading, eventually, to an "*Out of memory.*" error.

It's not clear why these declarations and calls have become an issue in Office 2016, for me at least, but these were the changes required.
As an aside the 'Default' email behaviour and default content in Office 2016 seem much improved (saved to 'Sent Items', Subject is just filename) and is probably the only option for OneDrive documents.

**[Modified Macro](https://gist.github.com/idiotandrobot/21fc665e652ffd53a81f):**

{% gist 21fc665e652ffd53a81f %}

**References**
- [Attachments.Add Method (Outlook)](https://msdn.microsoft.com/en-us/library/office/ff869553.aspx)
- [OlAttachmentType Enumeration (Outlook)](https://msdn.microsoft.com/en-us/library/office/ff868693.aspx)
