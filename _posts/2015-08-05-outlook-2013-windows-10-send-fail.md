---
layout: post
title: Outlook 2013 not sending emails since Windows 10 upgrade
tags: [windows10 outlook2013]
---
The solution suggested on various forums is to run 'sfc /scannow' from an Administrator Command Prompt and then restart Outlook.

In my case emails were sitting in the Outbox and the 'Outlook Send/Receive progress' dialog wasn't showing any errors.

I also had to open the email in question from the Outbox and hit 'Send' again.

## Opening an Administrator Command Prompt ##
1. Press the ['Windows' key](https://en.wikipedia.org/wiki/Windows_key)
2. Type 'cmd'
3. Right-click on 'Command Prompt (Desktop App)'
4. Select 'Run as administrator'
5. Click 'Yes' on the 'User Account Control' prompt
6. Type your command (in this case 'sfc /scannow')
