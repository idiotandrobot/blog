---
layout: post
title: This PC editor updated for Windows 10
tags: [windows10 thispc]
project: https://github.com/idiotandrobot/thispc
---
When Windows 8.1 came out `Computer` in the Windows Explorer Navigation Pane was renamed to `This PC` and a load of User folder links were added to it so instead of:-

`Computer`
- `Local Disk (C:)`
- `Local Disk (D:)`

You got:-

`This PC`
- `Desktop`
- `Documents`
- `Downloads`
- `Music`
- `Pictures`
- `Videos`
- `Local Disk (C:)`
- `Local Disk (D:)`

Which, to me at least, seemed a little cluttered, especially as there was already access via Libraries and they could always be added to Favourites if you didn't like/understand Libraries.

The worse part about this change was the lack of ability to customise the visibility of these links without going into the Registry. 
Having discovered the registry keys involved I wrote a [quick application]([[project]]) to provide a simple UI to rectify this oversight. 

Windows 10 has retained this Navigation Pane styling and (as far as I can tell) hasn't provided a way to customise it. What it has done is provided a second batch of registry keys to edit *in addition* to the original set.
These have now been added to the application and I can go back to my tidy Navigation Pane.
