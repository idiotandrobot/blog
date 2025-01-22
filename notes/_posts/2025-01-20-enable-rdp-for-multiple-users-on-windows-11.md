---
title: Enable RDP for multiple users on Windows 11
link: https://www.thewindowsclub.com/enable-rdp-for-multiple-users-on-windows-11
tags:
- RDP
- Windows 11
---
- Open `gpedit.msc` Local Group Policy Editor panel.
- Go to:-
  - `Computer Configuration`
    - `Administrative Templates`
      - `Windows Components`
        - `Remote Desktop Services`
          - `Remote Desktop Session Host`
            - `Connections`
- Set `Restrict Remote Desktop Services user to a single Remote Desktop Services session` policy to `Disabled`.
- Set `Limit number of connections` policy to `Enabled`.
  - Set the `RD Maximum Connections allowed` to `999999` (unlimited).
