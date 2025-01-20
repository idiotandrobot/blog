---
title: Enable RDP for multiple users on Windows 11
link: https://www.thewindowsclub.com/enable-rdp-for-multiple-users-on-windows-11
tags:-
- RDP
- Windows 11
---
- Open gpedit.msc Local Group Policy Editor panel.
- Go to Computer Configuration > Administrative Templates > Windows Components > Remote Desktop Services > Remote Desktop Session Host > Connections.
- Click on the ‘Restrict Remote Desktop Services’ user and change it to a single ‘Remote Desktop Services’ session policy and set it to Disabled.
- Click on the ‘Limit number of connections’ policy. The default state is ‘Not Configured.’ Select the Enabled radio button to enable the counter menu of ‘RD Maximum Connections’ permitted in the ‘Options’ section.
- Set the ‘RD Maximum Connections’ permitted to 999999.
- Click on OK to save the changes and Restart Windows.
