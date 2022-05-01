---
layout: post
tags: 
- C# 
- Dropbox 
- OneDrive
redirect_from: 
- /Windows-Cloud-Storage-Folder-Paths/
- /Cloud-Storage-Windows-Folder-Paths/
---
### [Dropbox](http://idiotandrobot.com/blog/dropbox-windows-folder-path/) ###

### OneDrive ###
The OneDrive folder path was originally stored in the registry under SkyDrive, but this is no longer the case.

Retrieving the contents of the `OneDriveConsumer` environment variable seems the most straightforward method.

{% gist 033fecaa13bb34cb622321333cd84a2c %}

via 

- [Stack Overflow: Get OneDrive path in Windows][1]

[1]:http://stackoverflow.com/questions/26771265/
