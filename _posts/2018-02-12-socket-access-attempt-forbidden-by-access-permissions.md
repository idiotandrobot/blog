---
layout: post
title: UWP use StreamSocket instead of TcpClient
category: post
tags:
- C#
- UWP
---
When accessing a remote port, from a UWP app, using TcpClient, an ExtendedSocketException *'An attempt was made to access a socket in a way forbidden by its access permissions'* is thrown.

References

- [TcpClient Class](https://msdn.microsoft.com/en-us/library/system.net.sockets.tcpclient)
- [StreamSocket Class](https://docs.microsoft.com/en-us/uwp/api/windows.networking.sockets.streamsocket)
- [UWP nativemessaging host print to network printer using sockets in C#
](https://stackoverflow.com/questions/47560323/uwp-nativemessaging-host-print-to-network-printer-using-sockets-in-c-sharp)
