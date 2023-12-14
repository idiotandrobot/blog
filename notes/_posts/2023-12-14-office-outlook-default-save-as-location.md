---
title: MS Office Outlook: Default Attachment Save-As Location
link: https://answers.microsoft.com/en-us/outlook_com/forum/all/office-outlook-2016-default-save-location-for/cad82586-2c24-4fbb-8906-e6661c25df00
tags:
- MS Office
- Outlook
- Registry
---
Add `DefaultPath` string value to `HKEY_CURRENT_USER\SOFTWARE\Microsoft\Office\16.0\Outlook\Options`. `%UserProfile%` works here.
