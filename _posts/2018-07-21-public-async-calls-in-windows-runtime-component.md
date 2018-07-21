---
layout: post
title: Using async keyword in windows runtime components
category: post
tags:
- C#
- UWP
- async/await
---
Creating a [background task](https://docs.microsoft.com/en-us/windows/uwp/launch-resume/support-your-app-with-background-tasks) for a UWP app requires a Windows Runtime Component to host the task (for [out-of-process background tasks](https://docs.microsoft.com/en-us/windows/uwp/launch-resume/create-and-register-a-background-task)).
Among the many requirements for creating Windows Runtime Components is the inability to expose [Task](https://docs.microsoft.com/en-us/dotnet/api/system.threading.tasks.task) as part of the signature of a public method.
i.e.

<noscript>
  <a href="https://gist.github.com/idiotandrobot/ca87bfb9d236e4103cdef75957289a59#file-dosomethingasync-cs">Gist: Do something async</a>
</noscript>
{% gist ca87bfb9d236e4103cdef75957289a59 dosomethingasync.cs %}

To get around this, the async method needs to be changed from public to internal/private (depending on local scope) and a public wrapper method provided.

<noscript>
  <a href="https://gist.github.com/idiotandrobot/ca87bfb9d236e4103cdef75957289a59#file-wrt_dosomethingasync-cs">Gist: Do something async valid for a Windows Runtime Component</a>
</noscript>
{% gist ca87bfb9d236e4103cdef75957289a59 wrt_dosomethingasync.cs %}

**References**

- [StackOverflow: Async Calls in UWP Background Application](https://stackoverflow.com/questions/45881751/async-calls-in-uwp-background-application)
- [MSDN: Exposing .NET tasks as WinRT asynchronous operations](https://blogs.msdn.microsoft.com/windowsappdev/2012/06/14/exposing-net-tasks-as-winrt-asynchronous-operations/)
- [Asynchronous programming with async and await (C#) - Return types and parameters](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/async/#BKMK_ReturnTypesandParameters)
- [Creating Windows Runtime Components in C# and Visual Basic - Asynchronous operations](https://docs.microsoft.com/en-us/windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic#asynchronous-operations)
