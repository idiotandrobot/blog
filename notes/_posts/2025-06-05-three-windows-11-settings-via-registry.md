---
title: Windows 11 Settings via Registry
link: https://www.howtogeek.com/registry-hacks-i-always-use-on-a-fresh-windows-11-install/
tags:
- Windows 11
---

- **Disable Bing Search in the Start Menu**
  - `Computer\HKEY_CURRENT_USER\SOFTWARE\Policies\Microsoft\Windows\Explorer`
    - DisableSearchBoxSuggestions (DWORD) = 1
- **Restore the Old Right-Click Context Menu**
  - `Computer\HKEY_CURRENT_USER\SOFTWARE\CLASSES\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32`
    - (Default) = 
- **Disable the Lock Screen**
  - `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\Personalization`
    - NoLockScreen (DWORD) = 1
