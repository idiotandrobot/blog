---
title: Wpf Could not load file or assembly System.Net.Sockets
tags: 
- WPF
- .NET Standard
links:
- [Runtime binding bug with .NET Standard Socket in a .NET Desktop Console App, https://forums.dotnetfoundation.org/t/runtime-binding-bug-with-net-standard-socket-in-a-net-desktop-console-app/2803]
- ["GitHub Issue: Dependencies don't flow from new NETStandard project to old Desktop projects through ProjectReferences #901", https://github.com/dotnet/sdk/issues/901]
---
Add to wpf project file
```
<PropertyGroup>
   <RestoreProjectStyle>PackageReference</RestoreProjectStyle>
</PropertyGroup>
```
