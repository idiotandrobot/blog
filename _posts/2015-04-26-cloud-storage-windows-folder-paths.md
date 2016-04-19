---
layout: post
tags: 
- C# 
- Dropbox 
- OneDrive
redirect_from: /Windows-Dropbox-Folder-Path/
redirect_from: /Windows-Cloud-Storage-Folder-Paths/
redirect_from: /Cloud-Storage-Windows-Folder-Paths/
---
<del>The Dropbox folder path is stored in host.db in the Dropbox ApplicationData/Local ApplicationData folders</del>. 
**Update:** See [How can I programmatically find the Dropbox folder paths?](http://idiotandrobot.com/blog/dropbox-windows-folder-path/)

{% gist dbe3f27e023b74b54d774ff07a03306f %}

The OneDrive folder path is stored in the registry under SkyDrive.

{% gist 033fecaa13bb34cb622321333cd84a2c %}

via 

- [Stack Overflow: How do I programmatically locate my Dropbox folder using C#?](http://stackoverflow.com/questions/9660280/)
- [Stack Overflow: Get OneDrive path in Windows](http://stackoverflow.com/questions/26771265/)
