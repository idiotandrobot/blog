---
layout: post
title: Resetting Ubuntu on Windows
tags: 
- Ubuntu on Windows
---
After you inevitably break your Windows Subsystem for Linux you can 'factory reset' it (including the file system) by running the following from an elevated Windows command prompt.

`lxrun /uninstall /full`

`lxrun /install`

via

- [How to remove/reset Windows Subsystem for Linux on Windows Insider Build 14316](http://superuser.com/questions/1065569/how-to-remove-reset-windows-subsystem-for-linux-on-windows-insider-build-14316)
