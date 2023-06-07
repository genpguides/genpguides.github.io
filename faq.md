---
order: 0
icon: question
---

# FAQ

!!!info This page might be partly outdated with current methods
!!!

!!!danger
**"adobegenp.com", "official-genp.com", "amtemu-adobe.com"** are not official and are fake websites.
**Please use only the links and information in this subreddit alone, for your own safety and our sanity.**
!!!

## What patching methods would work for me for x OS?

* **Windows:** Both GenP & M0nkrus
* **Mac:** Go to [r/AdobeZii](https://www.reddit.com/r/AdobeZii) or use [Cmacked](https://cmacked.com/)

## What is the official Discord server
[Official Discord server](https://discord.com/invite/X9ZuegSM4N)

## Can we downgrade the apps?
Downgrading adobe apps is not currently possible.

## What are latest versions of programs I can patch?
Check the [Update Compatibility List](https://www.reddit.com/r/GenP/comments/yao439/update_compatibility_list_2023_creative_suite/)

## What is GenP?
A script patcher that changes some things inside the directory of the apps programs so that it extends trial periods for undefinite time / download it without attachments.

## Is GenP safe?

* Many people either used or continue to use it. If there were was a problem we would know and remove the infected program. We have had no problem to date.

* Moderators do their best when something wild tries to spread here. You can also scan the program on [VirusTotal](https://www.virustotal.com/gui/) and [Hybrid Analysis](https://www.hybrid-analysis.com/). See and decide for yourself if you want to use it.

* Anti-Viruses tend to detect Patchers as viruses due to their behavior, however **GenP is a false positive**.

* If you wish, you can patch the programs and delete GenP from the PC after, as well scan your PC with [Malware Bytes](https://www.malwarebytes.com/).

## How to use GenP?

Check the [GenP Reddit Guide](https://www.reddit.com/r/GenP/wiki/redditgenpguides#wiki_guide_.232_-_dummy_guide_for_first_timers_genp_.28method_1.3A_cc.2Bgenp.29).
~~[OG Post - OUTDATED](https://www.reddit.com/r/GenP/comments/ktxsxk/genp_guide_installation_and_cleanup/)~~

<!-- - **GENP 2.7** - Outdated - There are two ways to patch a program: Automatic or Manual, and then clicking the Pill Picture.

> **Automatic:** Select the "CC 20xx" button (if you have default installation paths)

> The Automatic changed a bit since introduction 2023 versions, due to change of paths, needing to use the manual way to properly patch the apps.

> **Manual:** Select the app you want to patch (ideally one by one, so you don't mess up), find it's installation folder (usually "_C:\Program Files\Adobe_" for most apps and "_C:\Program Files (x86)\Adobe\Acrobat DC_" for Acrobat) and to select the file you need to patch **(it's name and extension is at the right bottom of File Explorer above Open and Cancel)**

&nbsp; -->

<!-- - **GENP 3.0** - This was the most needed and wanted update, since has new program language compared to 2.7 and is capable of finding all the necessary files automatically to properly patch with minimal work needed.

First Install the Programs (Pr / Ae / Ps, etc...).

- ### For patching apps in the default location:
    1. Press **Search Files** – wait until it finds all files.
    2. Press **Pill Button** – wait until it patches.
- ### For one app at a time:
    1. Press **Custom path** – select folder that you want [depends on the app you want to patch]
    2. Press **Search Files** - wait until it finds all files.
    3. Press **Pill Button** – wait until it patches. -->

### What is "File is not 'vanilla'. Aborting..."?

* **This is an error GenP gives you when you try to patch already patched file.** 

* To prevent this you can recover original file by finding a file ending with _.bak_ (for example _photoshop.exe.bak_), copying it so you don't lose the backup and renaming the copy to it's original name by removing _.bak_ from the end of it (to see file extensions you need to enable it in File Explorer by _View_ and ticking the box with _File name extensions_).

<!-- # [**Common Questions**](https://www.reddit.com/r/GenP/wiki/commonquestions) -->

## **GenP menu doesnt show after clicking "Runme.exe"**

If [this menu](https://i2.paste.pics/DGHAB.png) doesnt show up, few options:

- Turn antivirus Off, and try running again;

- If still not, open the "Resources" folder, and try running the "Adobe-
=GenP-2.7.exe"

- If neither those worked, move the WHOLE extracted GenP folder into a PenDrive and try launching GenP from the PenDrive, the menu should finally show up.

## **How to know if Patch worked or not?**
* When following the Guide #2:
    * In Creative Cloud (CC) you choose **"Start Trial" / "Try"** to download the apps you want, follow the guide blablabla.... and you patch everything.
    * When you open it will show you a **7 day trial banner, correct?** That will continue to countdown to zero, and change to "Your trial version is over" or something like that.

* Now, one of two things can will happen.
    * Trial is over and **you lose access** to the app, you cant use it without "buying". - **Patch Failed**
    * Trial is over but **you can still use** the app. - **Patch worked**

## **"File in not Vanilla"?**
* The app **is or was already patched**, its not an error. Meaning its working.

## **"Restart your ACC app manually. If it fails or you have problems with ...."?**
* **IT'S NOT A PROBLEM OR ERROR**. Whenever you run the patch to either Creative Cloud (CC) or the apps, it will show you that message every time. Think of it as **"I've completed the task, close me off and continue."**
* Just continue with the process until the end.

## **Trial counter?**
* If you were able to get the apps running with the patch but the counter still appears, do not fear. The counter will continue to count down but at zero the app will continue to work.
* If you are trying to install and shows TRIAL / TRY, its fine, just hit it and download the apps and continue the guide to patch the apps. - They will work
* You open the apps and says Trial 7days or less, its fine, if you patched it, it will continue to countdown, and at zero you will still be able to use it.

## **Can I update the app after I patched it?**
Yes you can, however you have to patch it again (usually). Before updating check [Update Compatibility List](https://www.reddit.com/r/GenP/?f=flair_name%3A%22Official%20Mod%20Post%22)

## **Neural filters do not work? ("Filter isn't available.")**
Just start the app as admin (worked in case of Photoshop).

## [**Acrobat (PDFMaker) is fighting with GenP?**](https://www.youtube.com/watch?v=vhK0hMQNPlM)
By u/k1ng_f1sh.

* Open Registry Editor (press Win + R, type "regedit" and press enter). Now go to:
* `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Adobe\Adobe Acrobat\DC\Activation`
* Right-click "_IsNGLEnforced_" and delete it, then create a new DWORD (32-bit) Value called "_IsAMTEnforced_" with a value of 1.
* Restart the PC and it should work.

## **Adobe Genuine Software Integrity ("...software you are using is not genuine.") pop-up window?**
Check [Disable AGSI for Wind/Mac](https://liuweishiwo0220.medium.com/how-to-disable-adobe-genuine-software-integrity-on-windows-mac-4c6cfac6809b).

## **Lightroom and Lightroom Classic don't work?**

For Lightroom you can try [this](https://www.reddit.com/r/GenP/comments/l15aop/real_lightroom_fix/) (if you have Lightroom already installed check the question above or you can simply reinstall, also you CAN NOT start the trial and if you already did, create a new account).
For Lightroom Classic try [this](https://www.reddit.com/r/GenP/comments/mec2j1/missing_option_to_roll_back_lightroom_classic/gsk45s7?utm_source=share&utm_medium=web2x&context=3) [(video)](https://youtu.be/vhK0hMQNPlM?t=52).

## **Program X doesn't work?**
Make a post about it and try to describe the problem, the more information we have the bigger chance is that someone finds a fix.

## **I patched a program and now it says "X trial days left | Buy now"?**
A good rule of thumb is that if it isn't a pop-up window it's fine.
Don't worry that's normal, the program will continue working after the "trial ends" (except Lightroom). There's a program called [HomeScreenFix](https://www.reddit.com/r/GenP/wiki/faq#wiki_homescreenfix) which removes the red trial button, however for it to work on latest versions it needs to be updated.

## **How can I downdate a program?**
We can't cuz of Adobe :c.
~~You can roll back in Creative Cloud app (however there's a limit and it's usually only few versions back while staying in the same CC 20xx). Simply find the app you want to downdate, three dots to the right from Open in All Apps section and there will be Other versions button and you can select the version you want. if you don't see some of the options go to _File_, _Preferences_, _Apps_, and at the bottom there will be setting _Show Older Apps_ (appears only after CC is patched).~~

## **Download older CC versions of a program?**

Use M0nkrus for standalone older versions of a program, CCMaker is no longer viable due to being infected with virus.

~~You can download original installers from [here](https://prodesigntools.com/tag/ddl).~~
~~You can also use [CCMaker](https://www.reddit.com/r/GenP/wiki/faq#wiki_ccmaker).~~
~~For versions older than 2019 you need AMTEmu.~~
~~Patching with AMTEmu is easy, turn it on, select program, find it's folder and select _amtlib.dll_ and done (sometimes there won't be a 2018 version in the dropdown menu, that's not a problem, select 2017 and it'll work).~~

## **How do I uninstall a program?**
You can go to Creative Cloud, _All apps_, _three dots_ to the right from the app you want to uninstall and _Uninstall_. You can also use this [official guide](https://helpx.adobe.com/creative-cloud/kb/cc-cleaner-tool-installation-problems.html) for cleanup, download is at the bottom. You can also uninstall apps from Windows control panel.

## **Change the language of an already installed app?**
You will have to change the language in _File_, _Preferences_, _Apps_ and reinstall the app.

# **Creative Cloud**
## **After reinstalling Creative Cloud some apps are missing.**
Just change the language in _File_, _Preferences_, _Apps_ to the one you've set before.

## **Creative Cloud loads too long?**
I don't have much information about this, but in my case, I either have to wait for [blue pop-ups](https://imgur.com/a/IDEaBOA) in the middle of the bottom part of the CC app, there are usually 2 or 3 at most, the last one has _Relaunch button_, after relaunch it works fine, you can kill all the processes manually using [Process Explorer](https://docs.microsoft.com/en-us/sysinternals/downloads/process-explorer) (you have to find and kill all [these](https://imgur.com/a/sZMrHaY)) or you can go to _File_ and _Exit_ and _Quit_.

## **After updating Creative Cloud all app updates are gone?**
I don't know how to fix this.

# What is HomeScreenFix?

* Fixes broken UI, where homepage of app would be all messed up and disconfigured

[Download: HomeScreenFix 4.0.2](https://www.reddit.com/r/GenP/comments/mt9m4f/adobe_home_screen_fix_402/).

Older Versions [4.0.1](https://www.reddit.com/r/GenP/comments/ltn2zw/adobe_home_screen_fix_401_newest_version/), [4.0.1](https://akvaithi.tk/index.php/s/9TBFnDBPjwj8o92), [3.5.8](https://www.reddit.com/r/GenP/comments/ky015a/new_homescreenfix_v358/).

## How to use HomeScreenFix?

* There are two ways,

1. Either put HomeScreenFix.exe (the name will be a bit different) into Resources folder (the folder is located in the same folder as RunMe.exe is) and GenP will automatically apply it while patching.

2. Simply start the exe, push the OK button at the bottom and it will do it's work.

# **AMTEmu** - *Before 2018 (OUTDATED)*
Older patcher abusing the vulnerabilities of amtlib.dll.

[Download: AMTEmu](https://appnee.com/amt-emulator/).

## **I can't find amtlib.dll**

* Make sure you are running program older than CC 2019 because after CC 2018 they changed the file system to stop AMTEmu vulnerabilities only to get introduced to GenP :D. If you still can't find amtlib.dll reinstall the program, this can sometimes happen.

# **CCMaker - Method 2**  - *Outdated & no longer supported due infested virus and many other operational problems*

[Download: CCMaker](https://appnee.com/ccmaker/).

!!!warning **This was dropped from use, and no longer recommended because after a certain version, there was probably an injection of viruses so we removed from the guides** and from recomending it to anyone. Not only that but there were several situations where 70% of the time it would say installation complete and nothing was installed, not to mention many broken apps.
!!!

* For 1.3.15 decrypt with AES `UnIAabmYU7yesFXwyCZGe3mRdYf6CF0x8gpeWrUr5ABa4J1alyZcAKUPjOUXcukLLSCaxaIJ1OncLKWQYQW8UQ==` key is _getblownaparteee_.

> All in one downloader, debloater and patcher (hopefully, if it doesn't work try patching with GenP). This program downloads the apps without requiring Creative Cloud.

> **Anti-virus goes completely mad with it**, we trusted Appnee but it's up to you to decide, there was no better source. The second download too has detections.


# What is **CCStopper**?

(thanks to u/TostiWee)

* A script that kills all CC processes (including apps), creates firewall rules, host patching, and disable / delete Adobe Genuine Service (AGS).

# What is **Acropolis**?

(thanks to u/Verix-)

* The script uses the official standalone Adobe Acrobat Pro installer and automatically patches it.

# * **End**

## **I have a problem which wasn't mentioned here**
Feel free to ask in the subreddit or in the Discord server.

## **Is Appnee safe?**

I personally trust them. The sites are moderated however still be cautious, rather be cautious than sorry. Official sites are free.appnee.com and appnee.com (they will be combined into just appnee.com soon).

## **Final notes**

If something isn't updated DM u/getblownaparte or u/allstart4u.