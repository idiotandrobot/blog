---
title: Mark .NET application to run as Administrator
gist: 0238019079641b0ac5f735e66edb5c8b
tags:
- Visual Studio
- .NET
- Windows
links:
- ["StackOverflow: How do I force my .NET application to run as administrator?",https://stackoverflow.com/questions/2818179/how-do-i-force-my-net-application-to-run-as-administrator]
- ["Designing UAC Applications for Windows Vista: Step 6",https://msdn.microsoft.com/en-us/library/bb756929.aspx]
- ["StackOverflow: UAC need for console application",https://stackoverflow.com/questions/227187/uac-need-for-console-application]
- ["StackOverflow: Difference between “highestAvailable” and “requireAdministrator” in manifest in terms of Elevation?
",https://stackoverflow.com/questions/12651124/difference-between-highestavailable-and-requireadministrator-in-manifest-in]
---
Add an app.manifest file to the Project and use the `System.Security.Principal` namespace to check at runtime whether privileges have been provided.
