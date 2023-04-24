---
title: Adding Context Menu Entries to Windows Explorer
tags:
- Registry
- Windows Explorer
links:
- https://www.advancedinstaller.com/forums/viewtopic.php?t=49822
---
Add registry entries for folder and background context menu items

## Folder Context Menu ##

### Root Key ###
`HKEY_LOCAL_MACHINE` or `HKEY_CURRENT_USER` - `\SOFTWARE\Classes\Directory\shell`

### New Keys/Values ###
1. Add new key `[MyAppName]` to root key, default data value: `Open With [MyAppName]`
2. Add new (Expandable) String Value `Icon` to **1**, data value `[Path to App exe/icon file]` 
3. Add `command` key to **1**, default data value `"[Path to App exe]" "%V"`

## Background Context Menu ##

### Root Key ###
`HKEY_LOCAL_MACHINE` or `HKEY_CURRENT_USER` - `\SOFTWARE\Classes\Directory\Background\shell`

### New Keys/Values ###
Add keys/values as per Folder Context Menu.
