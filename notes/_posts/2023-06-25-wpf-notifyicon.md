---
title: "StackOverflow: How to create WPF System Tray Icon when no \"Main\" host window exists"
link: https://stackoverflow.com/a/12677353/146360
tags:
- WPF
- NotifyIcon
gists:
- ["WPF NotifyIcon", 38ae2225f6ebc25676eb9e62aa82f38]
---
In .NET 5+ set `<UseWPF>true</UseWPF>` **and** `<UseWindowsForms>true</UseWindowsForms>` in the project file.
