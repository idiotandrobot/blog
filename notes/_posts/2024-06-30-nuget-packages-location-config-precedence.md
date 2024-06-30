---
title: NuGet Packages Location Settings Precedence
tags:
- NuGet
links:
- ["DEV: How to change default Nuget packages folder on Windows", https://dev.to/tombohub/how-to-change-default-nuget-packages-folder-on-windows-51hb]
- ["StackOverflow: Dotnet Nuget/package folder very big and for each user", https://stackoverflow.com/a/43962022/146360]
- ["MS Learn: Managing the global packages, cache, and temp folders", https://learn.microsoft.com/en-us/nuget/consume-packages/managing-the-global-packages-and-cache-folders]
- ["MS Learn: Common NuGet configurations", https://learn.microsoft.com/en-us/nuget/consume-packages/configuring-nuget-behavior]
- ["MS Learn: nuget.config reference: config section", https://learn.microsoft.com/en-us/nuget/reference/nuget-config-file#config-section]
---
1. `NUGET_PACKAGES` User environment variable
2. `NUGET_PACKAGES` System environment variable
3. `%APPDATA%\NuGet\NuGet.Config` file `config/globalPackagesFolder` setting
4. `%ProgramFiles(x86)%\NuGet\Config` file `config/globalPackagesFolder` setting

Check current location (new terminal needed for environmental variable change):-
`nuget locals global-packages -l`
