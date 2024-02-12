---
title: Keeping PowerShell Up-to-date
tags:
- PowerShell
links:
- [How to keep PowerShell Core up to date using Windows Terminal,https://tomssl.com/how-to-keep-powershell-core-up-to-date-using-windows-terminal/]
---
### Windows ###
<noscript>
  <a href="https://gist.github.com/5db6b2a7609c0470b9c17b1c83bd6ffb">Gist: Update Windows Powershell</a>
</noscript>
{% gist 5db6b2a7609c0470b9c17b1c83bd6ffb %}

### Windows Terminal ###
As per the link. Using the Settings UI to add a new profile, the correct format for the command line is:-
<noscript>
  <a href="https://gist.github.com/268fee704609a9348a116fdc64fcc783">Gist: Update Powershell using Windows Terminal Profile</a>
</noscript>
{% gist 268fee704609a9348a116fdc64fcc783 %}
   
### .Net Core only ###
<noscript>
  <a href="https://gist.github.com/147a7eb749297f965fa89c96ef432e7d">Gist: Update .NET Core Powershell</a>
</noscript>
{% gist 147a7eb749297f965fa89c96ef432e7d %}

N.B. This only updates PowerShell for .NET

### Via Visual Studio Code ###
- <del>Install ms-vscode.powershell extension.</del>
- <del>Integrated console will load and prompt to update if available.</del>
- <del>On MacOS, Homebrew may complain and require `brew upgrade --cask powershell` be run instead</del>

This method now redirects to the PowerShell github project, so no longer works as a "shortcut".
