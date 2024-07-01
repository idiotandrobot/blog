---
title: Nuget.Config
gist: bb1ef0b0c445c59b6b6e7d3537fb8814
tags:
- NuGet
links:
- ["MS Learn: Common NuGet configurations: How settings are applied", https://learn.microsoft.com/en-gb/nuget/consume-packages/configuring-nuget-behavior#how-settings-are-applied]
---
Set `repositoryPath` **and** `globalPackagesFolder` to ensure that all project references point to the new path. 
Environment variables need to be cleared as they'll override `Nuget.Config`.
