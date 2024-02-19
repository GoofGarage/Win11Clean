# Windows 11 23H2v2 Initial Setup

---

## 1.1 Boot from ISO or Flash Drive, Preparing Setup

As of this release, using ISO ___"Win11_23H2_<Language>_x64v2.iso"___ is the recommended starting point for new installations.

1. Ensure the following entries are selected:

   "Language to install": ***"English (United States)"*** _(or other preferred Language)_  
   "Time and currency format": ***"English (United States)"*** _(or other preferred Time and Currency formats)_  
   "Keyboard or input method": ***"US"*** _(or other preferred Keyboard Layout)_
2. Click the ***"Next"*** button.
3. Click the ***"Install now"*** button.

---

## 1.2 Windows Setup, Activate Windows
1. Enter your ***"Windows Product Key"***
2. Click the ***"Next"*** button.

---

## 1.3 Windows Setup, Applicable notices and license terms
1. Read the license terms and agreement if desired.  It will take ~8 minutes to read.
2. Check the box next to ***"I accept the Microsoft Software License Terms..."***
3. Click the ***"Next"*** button.

---

## 1.4 Windows Setup, Installation Type
1. Click the bottom entry, labeled ***"Custom: Install Windows only (advanced)"***

---

## 1.5 Windows Setup, Where to Install Windows
1. Ensure you can see your installed SSD as **Drive 0 Unallocated Space**, and that it is already selected.
  
   Its ***"Total size"*** and ***"Free space"*** should be as expected.  
   Storage is sold in units of 'gigabytes/GB' _(base 1000)_, but Windows displays file sizes and capacities in 'gebibytes/GiB' _(base 1024)_.  
   As a result, the ***"Total size"*** and ***"Free space"*** may be ~2.35% less than you may have anticipated.
2. Click the **"Next"** button.

   At this time, Windows will create a UEFI boot partition, a recovery partition, and will copy the installation files to local storage to be used by the rest of the installation process.
        
   This will take up to 3 minutes on a modern solid state drive.
4. Windows Setup will restart the computer in 10 seconds, or you can click the ***"Restart now"*** button.
   
   After restarting, Setup will continue.  
   It will then restart again during the process before allowing you to start configuring Windows for the first time.

---

## 1.6 Continue in "02_OOBE_SETUP.md"

---

The initial setup bootstrapping process has completed.  Move on to the next section in ***"02_OOBE_SETUP.md"***
