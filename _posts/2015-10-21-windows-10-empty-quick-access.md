---
title: Fixing Windows 10 File Explorer Quick access
tags: 
- Windows 10
---
My desktop pc stopped showing any contents for Quick access in File Explorer a couple of days ago. 
[Reddit](https://www.reddit.com/r/Windows10/comments/3f60l6/broken_quick_access/) provides various suggestions.

Deleting the contents of `%AppData%\Microsoft\windows\recent\automaticdestinations` causes the default pinned folders to reappear.

Subsequently deleting the contents of `%AppData%\Microsoft\windows\recent\customdestinations` doesn't seem to do anything.

Neither has caused recent files or folders to appear in the Navigation Pane.
