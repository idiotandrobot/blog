---
title: Construct your Windows app's icon
link: https://learn.microsoft.com/en-us/windows/apps/design/style/iconography/app-icon-construction#icon-scaling
tags:
- Windows
- Icons
---

| Windows 11 scale factor | 100% | 125% | 150% | 200% | 250% | 300% | 400% |
|:---|---:|---:|---:|---:|---:|---:|---:| 
| Context menu, title bar, system tray |	16px | 20px | 24px | 32px | 40px | 48px | 64px | 
| Taskbar, search results, Start all apps list | 24px | 30px | 36px | 48px | 60px | 72px | 96px | 
| Start pins | 32px | 40px | 48px | 64px | 80px | 96px | 256px | 

**Note**
```
Apps should have, at the bare minimum: 16x16, 24x24, 32x32, 48x48, and 256x256.

This covers the most common icon sizes, and by providing a 256px icon,
ensures Windows should only ever scale your icon down, never up.
```
