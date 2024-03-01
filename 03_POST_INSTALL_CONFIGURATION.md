# Windows 11 23H2v2 Post-Install Configuration

---

The default experience has a memory commit charge of ~1.8GB, and has ~124 running processes -- much leaner than 22H2v2!  
When we are done, we will have reduced this to a memory commit charge of ~1.7GB and ~110 running processes.  
We will do some cleanup to further trim things down most for the sake of improving privacy and reducing annoyances.    
Though there will also be a small measurable performance and power efficiency improvement.  

The post-installation guide covers the following topics:  

  * Only having Windows Update install updates when you choose to, and not automatically.

   This can prevent genuinely dangerous issues, like Windows automatically installing drivers that may prove unstable and leave you unable to boot back into Windows

  * Preventing Windows Update from automatically and forcibly restarting Windows without your explicit permission.  
  * Moving the Windows 11 Taskbar to be aligned to the left _(consistent with Windows 95 through Windows 10)_  
  * Removing "Suggestions" (adware) from the Start Menu and Notifications  
  * Disabling advertisements in Settings, File Explorer, and Notifications  
  * Disabling Telemetry that is sent to Microsoft, Advertisers and Third Parties  
  * Disabling Cortana and Copilot  
  * Removing pre-installed Bloatware applications that few ever find useful _(you may wish to remove more)_  
  * Improving security by having Windows Defender update more frequently, and using MAPS  

This will make Windows 11 more familiar, as well as eliminate data collection and a fair number of background tasks.
It will also reduce the initial commit charge of logging into the Explorer window manager to under 2GB of memory, which is roughly inline with Windows 10.

---

## 1.1 Post-installation: Windows Update

1. In the search box, type ***"Check for Updates"***, then click the, ***"Check for updates, System settings"*** best match.
2. Click the ***"Check for updates"*** button.

   It is likely that at least 5 updates will be found.  
   They will all start to install automatically.  This is intended.  
   The, ***"2024-02 Cumulative Update for Windows 11 Version 23H2 for x64-based Systems"*** will take the longest.  Possibly up to 15 minutes.  

3.  When all updates are Completed or Pending Restart, click the ***"Restart now"*** button.  

   The restart will take several minutes, and the post-restart update process will inform you of its progress.  

---

## 1.2 Post-installation: Windows Update, Part 2

1. You will need to log in to Windows with your username and password for the first time.
2. In the search box, type ***"Check for Updates"***, then click the, ***"Check for updates, System settings***" best match.
3. Click the ***"Check for updates"*** button.

   It is likely that at least 1 update will be found.  
   They will all start to install automatically.  This is intended.  

---

## 1.3 Post-installation: Windows Update, Part 3

Instead of installing any more updates (they should be done), we'll now customize how Windows 11 handles updates.  
We'll ensure that Windows only installs updates when you're ready, and won't forcibly restart your computer.

1. Click the ***"Advanced options"*** button, which is the 4th section from the top.
2. Set ***"Receive updates for other Microsoft products"*** _(first option from top)_ to ***"On"***.
3. Set ***"Notify me when a restart is required to finish updating"*** _(fourth option from top)_ to ***"On"***.
4. Close the "Settings" window.

## 1.3.1 Turn off Automatic Restarts

1. Press the ***"Windows Key + R"*** keyboard shortcut.
2. In the ***"Run"*** dialog enter, ***"gpedit.msc"*** then click the ***"OK"*** button.
3. In the "Local Group Policy Editor" window, navigate to the following path in the left sidebar:

  [Computer Configuration] > [Administrative Templates] > [Windows Components] > [Windows Update] > [Manage end user experience]  
  
5. In the right hand pane, double-click ***"Turn off auto-restart for updates during active hours"***.  Optionally also change the active hours.
6. On the ***"Turn off auto-restart for..."*** dialog, select ***"Enabled"***, then click the ***"OK"*** button.

## 1.3.2 Turn off Automatic Updating

Here we're going to disable the ability for Windows to automatically attempt to download and install updates.  
This is mostly recommended to guarantee system stability, but it will require you to update your computer yourself to stay secure.  
  
Microsoft generally releases patches on the 2nd Tuesday of the month.  This is known by IT professionals as, "Patch Tuesday".

# If you disable Automatic Updating, you should set a reminder for the 17th of every month, to remind yourself to install updates.

The 17th of the month is guaranteed to be at **LEAST** 72 hours after _"Patch Tuesday"_, giving ample time for Microsoft to pull problematic
updates, or for news to travel about how updates might adversely affect you, giving you time to make an informed decision.

1. In the right hand pane, double-click ***"Configure Automatic Updates"***
2. On the ***"Configure Automatic Updates"*** dialog, select ***"Disabled"*** then click the ***"OK"*** button.
3. Close the "Local Group Policy Editor" window.

---

## 2.1.1 Post-installation: Move Taskbar Icons to Left

For those used to having their Windows Start button and taskbar buttons aligned to the left, this will restore that behavior, as well as give you an opportunity to clean up the taskbar.

1. Right-click anywhere on the Windows Taskbar.
2. Click ***"Taskbar Settings"***
3. Click and expand ***"Taskbar behaviors"*** _(at the bottom of the right-hand side)_.
4. Change the ***"Taskbar alignment"*** to ***"Left"***.

## 2.1.2 Post-installation: Show Seconds in System Tray Clock

1. Click to enable the checkbox next to, ***"Show seconds in system tray clock (uses more power)."***

You may also want to disable Taskbar items such as ***"Task View"***, ***"Widgets"*** and ***"Chat"***, which can be found at the top of the window.  

2. Close the Settings window.

---

## 3.1 Post-installation: Customize Start Menu

1. In the search box, type ***"Start Settings"***, then click the, ***"Start Settings, System settings"*** match
2. Under ***"Layout"*** change from ***"Default"*** to ***"More pins"***.
3. You may wish to set ***"Show recently added apps"***, ***"Show recommendations for tips, shortcuts..."*** and ***"Show recently opened items..."*** to ***"Off"***.

---

## 3.2.1 Post-installation: Disable ads in the Settings app

1. Open the ***"Settings"*** app _(it should already be open)_.
2. Click on ***"Privacy & security"*** in the left-hand panel.
3. Click on ***"General"*** in the right-hand panel _(3rd from top)_.
4. Set ***"Let websites show me locally relevant content by accessing my language list"*** to ***"Off"***.
5. Set ***"Show me suggested contect in the Settings app"*** to ***"Off"***.
6. Close the "Settings" window.

## 3.2.2 Post-installation: Disable ads in the File Explorer

1. Open the [File Explorer].
2. Click the three horizontal dots ***"..."*** on the far right side of the menu bar
3. Click ***"Options"***.

4. Optionally uncheck, ***"Show frequently used folders"*** and ***"Show files from Office.com"*** if desired.

5. Open the ***"View"*** tab.
6. Uncheck ***"Show sync provider notifications"***.

7. The following are strong non-privacy-related suggestions, but are not required:

   Uncheck ***"Hide extensions for known file types"***.

8. Click the ***"Apply to Folders"*** button.  When prompted, click the ***"Yes"*** button.
9. Click the ***"OK"*** button to close the ***"Folder Options"*** dialog box.
10. Close "File Explorer".

## 3.2.3 Post-installation: Disable ads shown as Notifications
1. Open the ***"Settings"*** app.
2. Click on ***"System"*** in the left-hand pane.
3. Click on ***"Notifications"*** _(3rd from top)_ in the right-hand pane.
4. Click on the ***"Additional settings"*** button _(at the bottom)_ to expand it.
5. Uncheck, ***"Show the Windows welcome experience..."***.
7. Uncheck, ***"Get tips and suggestions when I use Windows"***.

## 3.2.4 Post-installation: Disable Suggestion Notifications in the Registry

This is required to completely disable Suggestion Toasts for things like Windows Co-Pilot Preview.  Unfortunately this must be repeated per user.

1. Press the ***"Windows Key + R"*** keyboard shortcut.
2. In the ***"Run"*** dialog enter, ***"regedit"*** then click the ***"OK"*** button.
3. Go to the following path: ***[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Notifications\Settings\Windows.SystemToast.Suggested]*** .
4. Double-click ***"Enabled"*** in the right pane
5. Ensure the value is set to ***"0"***.
6. Close the Registry Editor window.

---

## 3.3 Post-installation: Disable feedback requests 
1. Open the ***"Settings"*** app.
2. Click on ***"Privacy & security"*** in the left-hand pane.
3. Under ***"Diagnostics & Feedback"*** _(6th from the top)_, change the ***""Feedback frequency"*** to ***"Never"***.

---

## 3.4.1 Post-installation: Set time zone
1. Open the ***"Settings"*** app.
2. Click on ***"Time & language"*** in the left-hand pane.
3. Click ***"Date & time"*** in the right-hand pane.
4. Next to ***"Time zone"*** _choose the correct time zone for your location_.
5. Click the ***"Sync now"*** button under ***"Additional Settings"***

## 3.4.2 Post-installation: Disable Typing Insights

Typing Insights are stored on device and not set to Microsoft, but it represents a potential attack vector.  Power users may wish to disable them.

1. Open the ***"Settings"*** app.
2. Click on ***"Time & language"*** in the left-hand pane.
3. Click ***"Typing"*** _(3rd from the top)_ in the right-hand pane.
4. Click ***"Typing insights"*** _(6th from the top)_
5. Toggle ***"Typing insights"*** from On to ***"Off"***.

---

## 3.5.1 Post-installation: Disable Additional Diagnostic Data

1. Open the ***"Settings"*** app.
2. Click on ***"Privacy and Security"*** in the left-hand panel.
3. Click on ***"Activity History"*** _(7th from top)_ in the right hand pane.
4. Toggle, ***"Store my activity history on this device"*** from On to ***"Off].
5. Click the ***"Clear history""*** button under Clear Activity History, then click the ***"Clear"*** button.
6. Click the ***"<-"*** back arrow in the top-right hand corner of the "Settings" window.
7. Click on ***"General"*** _(3rd from top)_ in the right hand panel.
8. Close the "Settings" window.

## 3.5.2 Post-installation: Disable Data Collection

1. Press the ***"Windows Key + R"*** keyboard shortcut.
2. In the ***"Run"*** dialog enter, ***"regedit"*** then click the ***"OK"*** button.
3. Go to the following path: ***[HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\DataCollection]*** .
4. Click anywhere in the right pane, select ***"New"***, select ***"DWORD (32-bit)"*** and name it ***"AllowTelemetry"***.
5. Ensure the value of ***"AllowTelemetry"*** is set to ***"0"***.

## 3.5.3 Post-installation: Disable Windows Copilot in Registry

1. Go to the following path: ***[HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\]***
2. Click anywhere in the right pane, select ***"New"***, select ***"Key"*** and name it ***"WindowsCopilot"***.
3. Go to the following path: ***[HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\WindowsCopilot]*** 
4. Click anywhere in the right pane, select ***"New"***, select ***"DWORD (32-bit)"*** and name it ***"TurnOffWindowsCopilot"***.
5. Double click ***"TurnOffWindowsCopilot"***, set the value to ***"1"***, then click the ***"OK"*** button.
6. Close the "Registry Editor" window.

## 3.5.4 Post-installation: Disable Windows Copilot in Group Policy

1. Press the ***"Windows Key + R"*** keyboard shortcut.
2. In the ***"Run"*** dialog enter, ***"gpedit.msc"*** then click the ***"OK"*** button.
3. In the Local Group Policy Editor window, move to the following path in the left sidebar:

   [User Configuration] > [Administrative Templates] > [Windows Components] > [Windows Copilot]

4. In the right hand pane, double-click ***"Turn off Windows Copilot"***.
5. On the "Turn off Windows Copilot" dialog, select ***"Enabled"***, then click the ***"OK"*** button.
6. Close the "Local Group Policy Editor" window.

## 3.5.5 Post-installation: Disable Windows Copilot Preview in Taskbar

1. Open the ***"Settings"*** app.
2. Click on ***"Personalization"*** in the left-hand panel.
3. Toggle ***""Copilot (preview)"*** from On to ***"Off"***.

## 3.5.6 Post-installation: Disable the Telemetry Services

1. Press the ***"Windows Key + R"*** keyboard shortcut.
2. In the ***"Run"*** dialog enter, ***"services.msc"*** then click the ***"OK"*** button.
3. Double-click the ***"Connected User Experiences and Telemetry"*** service.
4. Click the ***"Stop"*** button to stop the service.
5. Set the ***"Startup Type"*** to ***"Disabled"***
6. Click the ***"OK"*** button to close the dialog.
7. Double-click the ***"Device Management Wireless Application Protocol (WAP) Push..."*** service.
8. Set the ***"Startup Type"*** to ***"Disabled"***.
9. Click the ***"OK"*** button to close the dialog.
10. Close the "Services" window.

## 3.5.7 Post-installation: Disable the Customer Experience Improvement Program

1. In the search box, search for ***"Task Scheduler"***, then click the ***"Task Scheduler app"*** match.
2. In the left-hand pane, navigate to [Task Scheduler Library] > [Microsoft] > [Windows] > then click on ***"Customer Experience Improvement Program"***.
3. In the middle pane, select _all items in the top grid view_, then click the ***"Disable"*** button in the bottom-right-hand pane labeled ***"Selected Items"***.
4. Close the "Task Scheduler" window.

--- 

## 3.6.1 Post-installation: Uninstall Cortana

1. Open the ***"Settings"*** app.
2. Click on ***"Apps"*** _(6th from top)_ in the left-hand pane.
3. Click on ***"Installed apps"*** _(top-most item)_ in the right-hand pane.
4. Find ***"Cortana""*** then click the ***"..."*** on the right, then click, ***"Uninstall"***.
5. Click the ***"Uninstall"*** button.

## 3.6.2 Post-installation: Disable Cortana in the Registry

1. Press the ***"Windows Key + R"*** keyboard shortcut.
2. In the ***"Run"*** dialog enter, ***"regedit"*** then click the ***"OK"*** button.
3. Go to the following path: ***[HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows]***
4. Right-click anywhere in the right-hand pane, click ***"New"*** > ***"Key"*** and name it ***"Windows Search"***
5. Right-click anywhere in the right-hand pane, click ***"New"*** > ***"DWORD (32-bit) Value"*** and name it ***"AllowCortana"***
6. Ensure the value of ***"AllowCortana"*** is set to ***"0"***.
7. Close the "Registry Editor" window

## 3.6.3 Post-installation: Disable Cortana in Group Policy

1. Press the ***"Windows Key + R"*** keyboard shortcut.
2. In the ***"Run"*** dialog enter, ***"gpedit.msc"*** then click the ***"OK"*** button.
3. In the Local Group Policy Editor window, move to the following path in the left sidebar:

   [Computer Configuration] > [Administrative Templates] > [Windows Components] > [Search]
   
4. In the right hand pane, double-click ***"Allow Cortana"***.
5. On the ***"Allow Cortana"*** dialog, select ***"Disabled"***, then click the ***"OK"*** button.
6. In the right hand pane, double-click ***"Allow Cortana above lock screen"***.
7. On the ***"Allow Cortana above lock screen"*** dialog, select ***"Disabled"***, then click the ***"OK"*** button.
8. In the right hand pane, double-click ***"Allow Cortana Page in OOBE on an AAD account"***.
9. On the ***"Allow Cortana Page in OOBE on an AAD account***" dialog, select ***"Disabled"***, then click the ***"OK"*** button.

## 3.6.4 Post-installation: Disable Web Search from Search Bar in Group Policy

1. Press the ***"Windows Key + R***" keyboard shortcut.
2. In the ***"Run***" dialog enter, ***"gpedit.msc***" then click the ***"OK***" button.
3. In the Local Group Policy Editor window, move to the following path in the left sidebar:
   
   [Computer Configuration] > [Administrative Templates] > [Windows Components] > [Search]
   
4. In the right hand pane, double-click ***"Allow search and Cortana to use location***".
5. On the ***"Allow search and Cortana to use location***" dialog, select ***"Disabled***", then click the ***"OK***" button.
6. In the right hand pane, double-click ***"Do not allow web search***".
7. On the ***"Do not allow web search"*** dialog, select ***"Enabled***", then click the ***"OK***" button.
8. In the right hand pane, double-click ***"Don't search the web or display web results in Search***".
9. On the ***"Don't search the web or display web results in Search"*** dialog, select ***"Enabled***", then click the ***"OK***" button.
10. In the right hand pane, double-click ***"Don't search the web or display web results in Search over metered connections***".
11. On the ***"Don't search the web or display web results in Search over metered connections"***, select ***"Enabled***", then click the ***"OK***" button.
12. In the right hand pane, double-click ***"Set what information is shared in Search***".
13. On the ***"Set what information is shared in Search"*** dialog, select ***"Enabled***", then select ***"Anonymous info***" for ***"Type of information***", then click the ***"OK***" button.

14. Close the "Local Group Policy Editor" window.

## 3.6.5 Post-installation: Disable Web Search from Search Bar in Registry

Yes, we genuinely have to do it here too.

1. Press the ***"Windows Key + R"*** keyboard shortcut.
2. In the ***"Run"*** dialog enter, ***"regedit"*** then click the [OK] button.
3. Go to the following path: ***[HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows]***
4. Right-click anywhere in the right-hand pane, click ***"New"*** > ***"Key"*** and name it ***"Explorer"***
5. Right-click anywhere in the right-hand pane, click ***"New"*** > ***"DWORD (32-bit) Value"*** and name it ***"DisableSearchBoxSuggestions"***
6. Ensure the value of ***"DisableSearchBoxSuggestions"*** is set to ***"1"***
7. Close the "Registry Editor" window

---

## 3.7 Post-installation: Update Search Permissions settings

1. Open the ***"Settings"*** app.
2. Click on ***"Privacy and Security"*** in the left-hand panel.
3. Click on ***"Search permissions"*** _(8th from top)_ in the right hand pane.
4. Set ***"Microsoft account"*** to ***"Off"***.
5. Set ***"Work or School account"*** to ***"Off"***.
6. Click the ***"Clear device search history"*** button.
7. Ensure ***"Show search highlights"*** is set to ***"Off"***.

---

## 3.8 Post-installation: Remove Widgets from Taskbar

1. Open the ***"Settings"*** app.
2. Click on ***"Personalization"*** in the left-hand panel.
3. Set ***"Widgets"*** to ***"Off"*** in the right-hand panel.

---

## 3.9 Post-installation: Restart to apply Group Policy setting changes

1. Restart the computer.

   Group Policy settings are applied when you log on.  Restarting will ensure all the Group Policy settings are applied.  

---

## 4.1.1 Post-installation: Set Terminal as default terminal application

The old "Command Line" application is now deprecated and will be removed in future versions of Windows.  Terminal is intended to entirely replace it.
Terminal is actually a really great, modern terminal application, including excellent integeration with WSL2, and great customization features.

1. In the search box, type ***"Terminal"***, then click the, ***"Run as administrator"*** on the right-hand side for the ***"Terminal App"***.
2. At the top of terminal, click ***"Open Settings"***.
3. Next to ***"Default terminal application"*** change the entry to ***"Windows Terminal"***.
4. Click the ***"Save"*** button.
5. Close the ***"Settings"*** application tab.  Do not close the entire window.

## 4.1.2 Post-installation: Remove Cortana

The terminal app should still be open if you only closed the "Settings" tab, and not the entire window.  If not...

1. In the search box, type "Terminal", then click the, [Run as administrator] on the right-hand side for the "Terminal App".
2. Type or copy-paste the following command:

```Get-AppxPackage -AllUsers *Microsoft.549981C3F5F10* | Remove-AppxPackage```

   If you wish to reinstall Cortana, you can reinstall it from the "Microsoft Store" application.  

## 4.1.3 Post-installation: Remove Other Applications, Part 1

The following applications are of marginal value to most people, so I will suggest removing them if you don't want them.  
Certainly if you use any of them, you should keep them.  These are also probably some of the best ways to use these services on Windows.  
If you want to add any of them back, you can do so from the ***"Microsoft Store"*** application.  

The Terminal app should still be open if you only closed the "Settings" tab, and not the entire window.  If not...

1. In the search box, type ***"Terminal"***, then click the, ***"Run as administrator"*** on the right-hand side for the ***"Terminal App"***.

2. If you want to save a full list of all Apps installed for all users, run this command, replacing **<USERNAME>** with your account's username.

   Typing or copy-pasting the following command will put a text file on your desktop named ***"Apps.txt"*** containing the output of the command.  

```Get-AppxPackage -AllUsers > C:\Users\<USERNAME>\Desktop\Apps.txt```

   You may wish to inspect this file yourself to ensure there's not anything new (not in the below list) that you want to remove.  
   Be careful about removing something made by Microsoft -- a lot of the stuff at the top may result in things breaking if you remove them.  
   The list below is 100% safe and nothing you're liable to ever miss.  

3. To remove any of the applications below, type or copy-paste the corresponding command into ***"Terminal"***, then press the ***"Enter"*** key on your keyboard.


   ***Bing News:***  
   
```Get-AppxPackage -AllUsers *Microsoft.BingNews* | Remove-AppxPackage```
	
   ***Clipchamp - Video Editor:***  
   
```Get-AppxPackage -AllUsers *Clipchamp.Clipchamp* | Remove-AppxPackage```

   Better free video editors exist, such as HitFilm Express.  You won't miss this one.  

   ***Office:***  
   
```Get-AppxPackage -AllUsers *Microsoft.MicrosoftOfficeHub* | Remove-AppxPackage```

   If you actually are installing Office, removing this won't hurt you.  You're much better off using the appropriate Office installer you plan to use.  

   ***Outlook:***  
   
```Get-AppxPackage -AllUsers *Microsoft.OutlookForWindows* | Remove-AppxPackage```

   Outlook syncs your sensitive credentials without your permission.  Yikes!  Strongly recommend not using Outlook in its current form.  

   ***People _(Address Book/Contact List)_:***  
   
```Get-AppxPackage -AllUsers *Microsoft.People* | Remove-AppxPackage```

   ***Solitaire _(only if you don't want Solitaire)_:***  
   
```Get-AppxPackage -AllUsers *Microsoft.MicrosoftSolitaireCollection* | Remove-AppxPackage```

   ***Teams:***  
   
```Get-AppxPackage -AllUsers *Microsoft.Teams* | Remove-AppxPackage```

   ***Windows Feedback Hub:***  
   
```Get-AppxPackage -AllUsers *Microsoft.WindowsFeedbackHub* | Remove-AppxPackage```

   ***Windows Maps:***  
   
```Get-AppxPackage -AllUsers *Microsoft.WindowsMaps* | Remove-AppxPackage```

   ***Zune Music:***  
   
```Get-AppxPackage -AllUsers *Microsoft.ZuneMusic* | Remove-AppxPackage```

   ***Zune Video:***  
   
```Get-AppxPackage -AllUsers *Microsoft.ZuneVideo* | Remove-AppxPackage```

## 4.1.4 Post-installation: Remove Other Applications, Part 2

These applications will only be removed for the current user.  You will need to repeat these for other users.  

All of these applications can be reinstalled from the ***"Microsoft Store"*** application if desired.  

1.	In the search box, type ***"Add or remove"***, then click the, ***"Add or remove programs"*** match.
2.	To remove an application, click the ***"..."*** button to the right-hand side of an application, then click ***"Uninstall"***.

The following apps are ones you may wish to remove, depending on your needs...

  * Clock

   _(this is not the Windows clock, it is a separate desktop clock application)_

  * Mail and Calendar

   _(if you have other applications you'd use for this functionality)_  
   
  * Microsoft OneDrive

   _(if you never plan to use OneDrive)_  
   
  * Microsoft Teams

   _(should already be gone)_  
    
  * Microsoft ToDo

   _(if you have other apps you use for ToDo lists and reminders)_  
   
  * Quick Assist
    
   _(if you will never allow others remote access to your computer for IT help desk purposes)_  
   
  * Sticky Notes

   _(virtual sticky notes.  some may want to keep this app around)_  
   
  * Tips
  * Voice Recorder

   _(if you don't want a Voice Recorder app)_  
   
  * Weather

   _(if you don't want Weather widgets)_  
   
  * Xbox Live

   _(if you do not intend to use Microsoft Game Pass functionality.  Always leave the other Xbox applications installed!)_  

## 4.1.5 Post-installation: Remove Other Applications, Part 3

These applications will only be removed for the current user.  You will need to repeat these for other users.

All of these applications can be reinstalled from the ***"Microsoft Store"*** application if desired.

1. Open the ***"Start"*** menu.
2. Right-click the Pinned application from the list below, then click the ***"Uninstall"*** menu option.

The following apps are ones you may wish to remove, depending on your needs...

  * Camo Studio  
  * ESPN  
  * Grammarly  
  * Instagram  
  * Kindle  
  * LinkedIn  
  * Luminar Neo - AI Photo Editor  
  * Messenger  
  * Netflix  
  * Outlook  
  * Prime Video  
  * Spotify  
  * TikTok  
  * WhatsApp  

---

## 4.2.1 Post-installation: Windows Deployment Image System Manager Cleanup

1. In the search box, type ***"Terminal"***, then click the, ***"Run as administrator"*** on the right-hand side for the ***"Terminal App"***.
2. Type or copy-paste the following command:

```dism /online /cleanup-image /startcomponentcleanup```

   This will clean up old versions of Windows components.  You have a fresh install, so this is just free real estate.  
   This may take several minutes (up to 10) to complete.  

3. Type or copy-paste the following command:

```dism /online /cleanup-image /analyzecomponentstore```

   This will inform you of how much space is still taken up by your local deployment image.  
   At this point it may be about 8GB, whereas in your initial installation it was closer to 20GB.

---

## 4.3.1 Post-installation: Update the Microsoft App Installer

1. In the search box, type ***"Store"***, then click the ***"Microsoft Store"*** match.
2. In the vertical menu along the left-hand side of the "Microsoft Store" window, click the ***"Library"*** button 2nd from the bottom _(above ***"Help"***)_
3. Scroll through the list on the right-hand side, then click on the ***"Update"*** button next to ***"App installer"***
4. After the App Installer app has updated successfully, close the "Microsoft Store" window.

---

## 4.4.1 Post-installation: Update the Windows App Installer from the Microsoft Store

PowerShell will get forcibly updated eventually, but you might as well take advantage of the newer version now.

1. In the search box, type ***"Terminal"***, then click the ***"Terminal"*** match.

2. Type or copy-paste the following command:

```winget install Microsoft.PowerShell```

3. Enter ***"Y"***, then press the ***ENTER*** key to agree to the source agreement for the Winget source.

Proceed with the installer.  

---

## 4.5.1 Post-installation: Install Alternative Web Browsers

It is likely you don't prefer Microsoft Edge.  Here's how to install browsers without ever having to even open Edge to install them.

1. In the search box, type ***"Terminal"***, then click the ***"Terminal"*** match.

2. Type or copy-paste any of the following commands to install the browser(s) of your choosing:

```winget install Mozilla.Firefox```  
```winget install Google.Chrome```

---

## 4.6.1 Post-installation: Change default web browser

1. In the search box, type ***"default"***, then click the, ***"Default apps, System Settings"*** match.
2. From the list, click either ***"Firefox"*** or ***"Google Chrome"***.
3. Click the ***"Set default"*** button at the top.
4. Scroll down to the ***".pdf"*** entry, then click it.
5. Choose either ***"Firefox"*** or ***"Google Chrome"*** as appropriate.  Then click the ***"Set default"*** button.

Repeat the previous two steps for the following entries:  

  * .htm
  * .html
  * .pdf
  * .shtml
  * .svg
  * .webp
  * .xht
  * .xhtml
  * HTTP
  * HTTPS

6. Close the "Settings" window.

---

## 4.7.1 Post-installation: Re-size Paging File

All operating systems will page things to disk eventually.  Eliminating a paging file entirely will eventually result in weird behavior and stability issues.

However, if you have plenty of memory, reducing the size of your paging file will free up some space.  
Moreover, ensuring your paging file is a fixed size will help to minimize fragmentation of memory paged to disk, improving performance.  

1. Open the ***"File Explorer***".
2. Right-click ***"This PC"*** in the left-hand pane, then click "Properties"***
3. Click the blue link, ***"Advanced system settings], which is the right-most link after, "Related Links"***.
4. Click the ***"Settings"*** button in the _"Performance"_ group.
5. Click the ***"Advanced"*** tab.
6. Click the ***"Change..."*** button in the _"Virtual memory"_ group.
7. Uncheck ***"Automatically manage paging file size for all drives"***.
8. Select the radio button, ***"Custom size"***.
9. Enter a value _(in MiB)_ for ***"Initial size (MB)"*** and ***"Maximum size (MB)"***.  These values should be identical.

   In general, this shouldn't be less than 4096MB for a modern system.  
   If you want the ability to record a memory dump in a crash, this should be a minimum of: _(GB of installed memory * 1024) + 4096_  

10. Click the ***"Set"*** button.
11. Click the ***"OK"*** button.
12. You will be notified that you need to restart Windows for the change to take effect.  Click the ***"OK"*** button.
13. Close all of the remaining Windows.  
14. Click the ***"Restart Now"*** button.

---

## 5.1.1 Windows 11 Hardening: Enable MAPS

1. Press the ***"Windows Key + R"*** keyboard shortcut.
2. In the ***"Run"*** dialog enter, ***"gpedit.msc"*** then click the ***"OK"*** button.
3. In the Local Group Policy Editor window, move to the following path in the left sidebar:

   [Computer Configuration] > [Administrative Templates] > [Windows Components] > [Microsoft Defender Antivirus] > [MAPS]  
   
4. In the right hand pane, double-click ***"Join Microsoft MAPS"***.
5. On the "Join Microsoft MAPS" dialog, select ***"Enabled"***, then set ***"Join Microsoft MAPS***" to ***"Advanced Maps"***.
6. Click the ***"OK"*** button to close the "Join Microsoft MAPS" dialog.

## 5.1.2 Windows 11 Hardening: Enable Block at First Sight

1. In the right hand pane, double-click ***"Configure the 'Block at First Sight' feature"***.
2. On the "Configure the 'Block at First Sight' feature" dialog, select ***"Enabled"***.
3. Click the ***"OK"*** button to close the "Configure the 'Block at First Sight' feature" dialog.

## 5.1.3 Windows 11 Hardening: Configure MAPS reporting

1. In the right hand pane, double-click ***"Configure local setting override for reporting to Microsoft MAPS"***.
2. On the "Configure local setting override for reporting to Microsoft MAPS" dialog, select ***"Enabled"***.
3. Click the ***"OK"*** button to close the "Configure local setting override for reporting to Microsoft MAPS" dialog.

## 5.1.4 Windows 11 Hardening: Configure MAPS Sample File policy

1. In the right hand pane, double-click ***"Send file samples when further analysis is required"***.
2. On the "Send file samples when further analysis is required" dialog, select ***"Enabled"***, then set ***"Send file samples when further analysis is required"*** to ***"Send safe samples"***.
3. Click the ***"OK"*** button to close the "Send file samples when further analysis is required" dialog.

---

## 5.2.1 Windows 11 Hardening: Enable Windows Defender Cloud Protection

1. In the Local Group Policy Editor window, move to the following path in the left sidebar:

   [Computer Configuration] > [Administrative Templates] > [Windows Components] > [Microsoft Defender Antivirus] > [MpEngine]

2. In the right hand pane, double-click ***"Select cloud protection level"***.
3. On the ***"Select cloud protection level"*** dialog, select ***"Enabled"***, then set ***"Select cloud blocking level"*** to ***"High blocking level"***.
4. Click the ***"OK"*** button to close the "Select cloud protection level" dialog.

## 5.2.2 Windows 11 Hardening: Set Cloud Protection Check Time Limit

1. In the right hand pane, double-click ***"Configure extended cloud check"***.
2. On the "Configure extended cloud check" dialog, select ***"Enabled"***, then set ***"Specify the extended cloud check time in seconds"*** to ***"50"***.
3. Click the ***"OK"*** button to close the "Configure extended cloud check" dialog.

4. Close the "Local Group Policy Editor" window.

---

## 5.3.1 Restart Computer

1. You must restart Windows for the above changes to take effect.

   This is required to complete the rest of the security hardening configuration.  

## 5.4.1 Windows 11 Hardening: Set a More Aggressive Windows Defender Signature Update Interval

1. In the search box, type ***"Terminal"***, then click the, ***"Run as administrator"*** on the right-hand side for the ***"Terminal App"***.
2. Type or copy-paste the following command:

```Set-MpPreference -SignatureUpdateInterval 1```  

## 5.4.2 Windows 11 Hardening: Configure Windows Defender to update signatures before a scan starts

1. Type or copy-paste the following command:

```Set-MpPreference -CheckForSignaturesBeforeRunningScan 1```

2. Close the Terminal application window.

## 5.5.1 Windows 11 Hardening: Improve Exploit Protection Defaults

1. In the search box, type ***"Windows Security", then click the, ***"Windows Security, System Settings"*** match.
2. Click the ***"App & browser control"*** entry in the left-hand pane.
3. Click the blue link, ***"Exploit protection settings"*** in the right-hand pane under "Exploit Protection".
4. Under ***"System Settings"*** _(default tab)_, ensure ***"Use default (On)"*** is set for all entries.

## 5.5.2 Windows 11 Hardening: Install Microsoft Defender Application Guard for Microsoft Edge

This significantly hardens Microsoft Edge, turning off many of its features in the sake of security.  
These features can always be turned back on -- if you want them back on -- for Microsoft Edge.  
Consider this section completely optional.  Yet if you'd like Edge to exist purely as a hyper-secure browser, consider it.  

1. Click ***"App & browser control"*** from the left-hand pane of the "Windows Security" window.
2. Click the ***"Install Microsoft Defender Application Guard"*** blue link in the right-hand pane under, ***"Isolated browsing."***
3. In the "Windows Features" dialog, check ***"Microsoft Defender Application Guard"***, click the ***"Yes"*** button when prompted to confirm the change, then click the ***"OK***" button.

## 5.5.3 Restart Computer

1. You must restart Windows for the above changes to take effect.
   
   This is required to complete the rest of the security hardening configuration.

---

## 6.1 Guide Complete

This concludes the current version of the ***Win11Clean*** guide.  The next planned release is in June 2024.

If you found this guide useful, please share the following link with friends and colleagues: [https://github.com/GoofGarage/Win11Clean](https://github.com/GoofGarage/Win11Clean)
