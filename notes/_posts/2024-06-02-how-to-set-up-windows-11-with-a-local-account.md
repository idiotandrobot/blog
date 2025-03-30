---
title: How to set up Windows 11 with a local account
tags:
- Windows 11
- Microsoft
---
During Windows setup:-
1. <kbd>Shift</kbd> + <kbd>F10</kbd> to open command prompt.
2. `>oobe\bypassnro`
3. Setup will restart with "*I don't have internet*" option at network selection.

<!--
Notes
- https://www.windowscentral.com/software-apps/windows-11/microsoft-will-force-windows-11-installs-to-use-a-microsoft-account-confirms-removal-of-popular-setup-bypass
- `>reg add HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\OOBE /v BypassNRO /t REG_DWORD /d 1 /f shutdown /r /t 0`
- https://www.windowscentral.com/software-apps/windows-11/an-even-better-microsoft-account-bypass-for-windows-11-has-already-been-discovered
- `>start ms-cxh:localonly`
-->
