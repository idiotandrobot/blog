---
layout: post
title: sudo&#58; unable to to resolve host error
tags: 
- Ubuntu on Windows
---
On all my Ubuntu on Windows installs to date I've initially got a `sudo: unable to resolve host <PCNAME>` error when running a command with sudo.

The problem is that, although the PC name has been added to /etc/hostname, an entry for it has not added to /etc/hosts.
The default /etc/hosts seems to just contain an entry for localhost on 127.0.0.1.
It also needs an entry for <PCNAME> on 127.0.1.1, where <PCNAME> is the value found in /etc/hostname.

via

- [Error message when I run sudo: unable to resolve host (none)](http://askubuntu.com/questions/59458/error-message-when-i-run-sudo-unable-to-resolve-host-none)
- [What is difference between localhost address 127.0.0.1 and 127.0.1.1](http://askubuntu.com/questions/754213/what-is-difference-between-localhost-address-127-0-0-1-and-127-0-1-1)
