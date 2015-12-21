---
layout: post
title: This PC editor updated for Windows 10
tags: 
- Windows 10 
- This PC
---
When Windows 8.1 came out `Computer` in the Windows Explorer Navigation Pane was renamed to `This PC` and a load of User folder links were added to it.

So instead of:-

- `Computer`
  - `Local Disk (C:)`
  - `Local Disk (D:)`

You got:-

- `This PC`
  - `Desktop`
  - `Documents`
  - `Downloads`
  - `Music`
  - `Pictures`
  - `Videos`
  - `Local Disk (C:)`
  - `Local Disk (D:)`

Which, to me at least, seemed a little cluttered, especially as there was already access via Libraries and they could always be added to Favourites if you didn't like/understand Libraries.

The worst part about this change was the lack of link visibility customisation available without going into the Registry. 
Having discovered the various registry keys involved I wrote a [quick application](https://github.com/idiotandrobot/thispc) to provide a simple UI to rectify this oversight. 

Windows 10 has retained this Navigation Pane styling and (as far as I can tell) hasn't provided a way to customise it. What it has done is provided a second batch of registry keys to edit *in addition* to the original set.
These have now been added to the application and I can go back to my tidy Navigation Pane.
