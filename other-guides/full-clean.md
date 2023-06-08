---
order: -1
# icon: trash
---

# Full Clean: Nothing is working

## Video Tutorial
(0 to 7:20 only)
[!embed](https://youtube.com/embed/jezUElhqrRA)

## Downloads :icon-download:

- [Download: Creative Cloud CLEANER TOOL](https://helpx.adobe.com/creative-cloud/kb/cc-cleaner-tool-installation-problems.html)

If you been having or continue to have issues overall.
I'd advise to remove everything adobe related, and start all fresh.

!!!warning ATTENTION 
Any brushes, plugins or other assets you may have installed will be deleted. Export and save them into a folder in your desktop.
!!!

## Procedure 

### 1. Remove any trace of ALL Adobe  
   1. Run Adobe Cleaner Tool in **ALL** | *(E, Y, 1, Clean All, Y)*  
   2. Check Windows Control Panel > Uninstall, and see if the app was removed successfully, otherwise remove it there manually.  
   
### 2. Delete Adobe folders from your disk, usually "C:\"
   - `Program files`
   - `Program files\common files`
   - `Program files x86`
   - `Program files x86\common files`
   - `%appdata%`
   - `appdata\local`
   - `appdata\local\temp`
   - `appdata\roaming`
   
### 3. Registry Editor
   1. Windows key, write "registry editor" should show up
   2. On `HKEY_CURRENT_USER` and `HKEY_LOCAL_MACHINE`  
    Look for **Software** and delete **Adobe**.

### 4. Remove Windows Firewall rules or Host File lines
   **For Windows Firewall**
   - Go to `Windows > Windows Firewall > Advanced Settings`
   - Check both in **Inbound** and **Outbound**
   - Remove or disable any rules blocking adobe processes or services, could be named with CCStopper or any other name you gave them.
   - If you created these in your AntiVirus, you'll have to do the same there.

   **For Host File**
   - Go to `%WinDir%\System32\Drivers\Etc`
   - Right-click on "**hosts**" file, "Open with notepad" and remove all the lines related to "# BLOCK ADOBE #" in this post, save the file and reboot your system:

```DEFAULT HOST LINES - You can copy-and-paste it
# Copyright (c) 1993-2009 Microsoft Corp.
#
# This is a sample HOSTS file used by Microsoft TCP/IP for Windows.
#
# This file contains the mappings of IP addresses to host names. Each
# entry should be kept on an individual line. The IP address should
# be placed in the first column followed by the corresponding host name.
# The IP address and the host name should be separated by at least one
# space.
#
# Additionally, comments (such as these) may be inserted on individual
# lines or following the machine name denoted by a '#' symbol.
#
# For example:
#
#      102.54.94.97     rhino.acme.com          # source server
#       38.25.63.10     x.acme.com              # x client host

# localhost name resolution is handled within DNS itself.
#	127.0.0.1       localhost
#	::1             localhost

```

### 5. Restart the PC

Adobe should not be in your system, and if you install it again it will behave normally 🙂 