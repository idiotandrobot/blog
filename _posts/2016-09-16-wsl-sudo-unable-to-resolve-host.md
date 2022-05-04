---
title: sudo&#58; unable to to resolve host error
tags: 
- Ubuntu on Windows
links:
- ["Error message when I run sudo: unable to resolve host (none)",http://askubuntu.com/questions/59458/error-message-when-i-run-sudo-unable-to-resolve-host-none]
- [What is difference between localhost address 127.0.0.1 and 127.0.1.1,http://askubuntu.com/questions/754213/what-is-difference-between-localhost-address-127-0-0-1-and-127-0-1-1]
- [Error 0x80070490 after modifying /etc/hosts from Windows,https://github.com/Microsoft/BashOnWindows/issues/735]
---
On all my Ubuntu on Windows installs to date I've initially got a `sudo: unable to resolve host [PCNAME]` error when running a command with sudo.

The problem is that, although the PC name has been added to /etc/hostname, an entry for it has not added to /etc/hosts.

The default /etc/hosts seems to just contain an entry for localhost on 127.0.0.1.

It also needs an entry for [PCNAME] on 127.0.1.1, where [PCNAME] is the value found in /etc/hostname.

**NB**
Modifying files inside of %localappdata%\lxss from Windows is not supported in WSL. It seems you can *just* about get away with editing /etc/hosts in Notepad but not Notepad++, otherwise you'll see an Error 0x80070490 when trying to run Bash from the Command Prompt and a rapidly closing window if you try and run it from Start. 

**TL:DR**
The best way of resolving this is to delete /etc/hosts and the next Bash session will autogenerate a file with the correct contents.
