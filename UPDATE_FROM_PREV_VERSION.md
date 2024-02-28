# Windows 11 23H2v2 Updating from Previous Guide Versions

---
Use this section only if you're updating from a previous release of the Win11Clean Guide.  This document is culled down to only contain the changes from the previous release to be current, for all releases from 0.4.2 onwards.

---

# 0.4.2 from 0.3.0

## 1. Post-installation: Disable ads shown as Notifications
1. Open the ***"Settings"*** app.
2. Click on ***"System"*** in the left-hand pane.
3. Click on ***"Notifications"*** _(3rd from top)_ in the right-hand pane.
4. Click on the ***"Additional settings"*** button _(at the bottom)_ to expand it.
5. Uncheck, ***"Show the Windows welcome experience..."***.
7. Uncheck, ***"Get tips and suggestions when I use Windows"***.

## 2. Post-installation: Disable Windows Copilot in Group Policy

1. Press the ***"Windows Key + R"*** keyboard shortcut.
2. In the ***"Run"*** dialog enter, ***"gpedit.msc"*** then click the ***"OK"*** button.
3. In the Local Group Policy Editor window, move to the following path in the left sidebar:

   [User Configuration] > [Administrative Templates] > [Windows Components] > [Windows Copilot]

4. In the right hand pane, double-click ***"Turn off Windows Copilot"***.
5. On the "Turn off Windows Copilot" dialog, select ***"Enabled"***, then click the ***"OK"*** button.
6. Close the "Local Group Policy Editor" window.

## 3. Post-installation: Disable Windows Copilot Preview in Taskbar

1. Open the ***"Settings"*** app.
2. Click on ***"Personalization"*** in the left-hand panel.
3. Toggle ***""Copilot (preview)"*** from On to ***"Off"***.
