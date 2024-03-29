# Windows 11 23H2v2 Out-of-Box Experience (OOBE) Setup

---

## 1.1 Out of Box Experience, Country/Region

1. When prompted, ***"Is this the right country or region?"***, ensure ***"United States"*** _(or the country you live in)_ is selected.
2. Click the ***"Yes"*** button.

---

## 1.2 Out of Box Experience, Keyboard Layout/Input Method

1. When prompted, ***"Is this the right keyboard layout or input method?"***, ensure ***"US"*** _(or the keyboard layout you prefer)_ is selected.
2. Click the ***"Yes"*** button.
3. When prompted, ***"Want to add a second keyboard layout?"***, click the ***"Skip"*** button.

---

## 1.3 Out of Box Experience, Hostname

1. When prompted ***"Let's name your device"*** enter a hostname in the [Name your device] text box.

   This will be the _DNS hostname_ and _legacy NETBIOS name_ of your computer.  
   This is very relevant outside of the most basic home network setups.  
   You can always change this later.  

2. Click the ***"Next"*** button.
3. Setup will restart.  After restarting, Setup will continue.  
  
---

## 2.1 Out of Box Experience, Set Up


# THIS IS ONE OF THE MOST IMPORTANT STEPS TO AVOID WHAT EVERYONE COMPLAINS ABOUT WITH WINDOWS 11!

1. When prompted, ***"How would you like to set up this device?"***, select ***"Set up for work or school"***.

   You will not be setting this up 'for work or school'.  
   What this choice does, is **it tells Microsoft that you do not want to log in or require a Microsoft account** to use the computer.  
   You will handle authentication on your own, whether that's through local authentication that is wholly managed by your computer _(what most home users would expect)_, or an Active Directory or LDAP account with an organization _(businesses or homelab users)_.

   In your case, you'll have local accounts that only exist on this computer.  
   If you have a complex network setup, you might have LDAP directory services, or other authentication services running on a server.

2.  Click the ***"Next"*** button.

---

## 2.2 Out of Box Experience, Sign-in Options

# THIS IS ONE OF THE MOST IMPORTANT STEPS TO AVOID WHAT EVERYONE COMPLAINS ABOUT WITH WINDOWS 11!

1. When prompted, ***"Let's set things up for your work or school"***, click the blue ***"Sign-in options"*** link underneath the _"Sign in"_ textbox.
2. Select, ***"Domain join instead"***.

   You will not be joining a Windows Active Directory domain, but _this option ensures you are not required to use a Microsoft Account_.

---

## 2.3 Out of Box Experience, Local Account Username

# THIS IS ONE OF THE MOST IMPORTANT STEPS TO AVOID WHAT EVERYONE COMPLAINS ABOUT WITH WINDOWS 11!

1. When prompted, ***"Who's going to use this device?"*** enter a username for the local account in the ***"Enter your name"*** textbox.

   This is an authentication username, and is not intended to be a person's full name.  
   Ensure this username makes sense to you.  It's the user you'll select (or enter) when logging in to Windows.  
   In basic home networking setups,  this might be the username you use when connecting to resources shared by this computer.  

2. Click the ***"Next"*** Button.

--- 

## 2.4 Out of Box Experience, Local Account Security

# THIS IS ONE OF THE MOST IMPORTANT STEPS TO AVOID WHAT EVERYONE COMPLAINS ABOUT WITH WINDOWS 11!

1.  When prompted, ***"Create a super memorable password"***, enter a password.

  * Passphrases are generally recommended as their longer length significantly increases entropy.  
   _Consider a short sentence you'd never forget in your life_, and include all proper capitalization, spaces, punctuation and numbers.  
   For example, ***"My favorite 3rd Grade teacher was Mr. Jabroni!"***  

  * You should use a Password Manager such as ***BitWarden***, ***KeePassXC*** or ***1Password*** to manage your passwords.

  * **KeePassXC** is easy to self-host, manage and synchronize across your devices. 

  * **BitWarden** managing your vault is very easy to set up, and is free, but it means you do not have complete control of your data.
    BitWarden can be complex to self-host, but is a genuine and highly-regarded enterprise-grade solution.

  * **1Password** no longer can be wholly self-managed past Version 7.x.  
   1Password is a very highly-regarded enterprise-grade solution, but not free, and you do not have complete control of your data.

2.	Click the ***"Next"*** Button.

3.	When prompted, ***"Confirm your password"***, re-enter the password.

	Ensure you are entering your password based on what you recorded in your existing password manager.
	If you can't confirm it successfully here, click the ***"<-"*** in the upper left-hand corner of the window to go back to the previous screen.

4.	Click the ***"Next"*** Button.

5.	When prompted, ***"Now add security questions"***, select ***"Security question (1 of 3)"***.
	Enter an answer in the textbox labeled ***"Your answer"***.

	Security questions and answers can also be stored with all the other account information in your password manager.

6.	Click the ***"Next"*** Button.

7.	When prompted, ***"Now add security questions"***, select ***"Security question (2 of 3)"***.
	Enter an answer in the textbox labeled ***"Your answer"***.

8.	Click the ***"Next"*** Button.

9.	When prompted, ***"Now add security questions"***, select ***"Security question (3 of 3)"***.
	Enter an answer in the textbox labeled ***"Your answer"***.

10.	Click the ***"Next"*** Button.

---

## 2.5 Out of Box Experience, Privacy Settings

It is recommended to disable all of the following settings.  You can always selective enable them again later in the Windows 11 "Settings" application.

1. When prompted, "Choose privacy settings for your device"...

  * Change ***"Location"*** to ***"No"***.
  * Change ***"Find my device"*** to ***"No"***.
  * Change ***"Diagnostic data"*** to ***"Required only"***.
  * Change ***"Inking & typing"*** to ***"No"***.
  * Change ***"Tailored experiences"*** to ***"No"***.
  * Change ***"Advertising ID"*** to ***"No"***.

2. Click the ***"Accept"*** Button.

   Setup will restart.  This will create your user profile and finish configuring Windows.
   When completed, it will automatically log into your account _(just this once)_ and you'll enter the typical Windows 11 "Explorer" window manager experience.

   Subsequent reboots will require your password as you would normally expect.

--- 

## 2.6 Continue in "03_POST_INSTALL_CONFIGURATION.md"

The initial setup bootstrapping process has completed.  Move on to the next section in ***"03_POST_INSTALL_CONFIGURATION.md"***.  

The next section is the bulk of the guide, and where you will customize Windows 11.
