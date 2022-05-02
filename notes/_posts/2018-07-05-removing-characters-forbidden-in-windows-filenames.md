---
title: Removing characters which are not allowed in Windows filenames
category: link
tags: 
- Windows
- Regex
links: https://www.codeproject.com/Tips/758861/Removing-characters-which-are-not-allowed-in-Windo
---
Regex illegalInFileName = new Regex(@"[\\/:*?""<>|]");
string myString = illegalInFileName.Replace(myString, "");

Removing characters which are not allowed in Windows filenames
