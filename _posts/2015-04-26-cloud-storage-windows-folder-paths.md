---
tags: 
- C# 
- Dropbox 
- OneDrive
links:
- ["Stack Overflow: Get OneDrive path in Windows",http://stackoverflow.com/questions/26771265/]
redirect_from: 
- /Windows-Cloud-Storage-Folder-Paths/
- /Cloud-Storage-Windows-Folder-Paths/
---
### [Dropbox]({{ site.baseurl }}{% link _posts/2016-04-16-dropbox-windows-folder-path.md %}) ###

### OneDrive ###
The OneDrive folder path was originally stored in the registry under SkyDrive, but this is no longer the case.

Retrieving the contents of the `OneDriveConsumer` environment variable seems the most straightforward method.

{% gist 033fecaa13bb34cb622321333cd84a2c %}

