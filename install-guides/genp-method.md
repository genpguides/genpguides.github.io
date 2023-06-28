---
order: 10
---

<!-- Links  -->
[5]: https://www.reddit.com/r/GenP/comments/yao439/update_compatibility_list_2023_creative_suite/

[8]: https://www.reddit.com/r/GenP/comments/mt9m4f/adobe_home_screen_fix_402

[9]: https://github.com/eaaasun/CCStopper/releases
[10]: https://helpx.adobe.com/creative-cloud/kb/cc-cleaner-tool-installation-problems.html
[11]: https://creativecloud.adobe.com/apps/download/creative-cloud
[12]: https://www.mediafire.com/file/3lpsrxiz47mlhu2/Adobe-GenP-2.7.zip/file
[13]: https://www.revouninstaller.com/

[15]: https://w14.monkrus.ws/search?q=Adobe+Lightroom+Classic&max-results=20&by-date=true

[17]: https://www.qbittorrent.org/download.php
[18]: https://w14.monkrus.ws/search?q=Adobe+Photoshop&max-results=20&by-date=true
[19]: https://w14.monkrus.ws/search?q=Adobe+Illustrator&max-results=20&by-date=true
[20]: https://w14.monkrus.ws/search?q=Adobe+Premiere+Pro&max-results=20&by-date=true
[21]: https://w14.monkrus.ws/search?q=Adobe+After+Effects&max-results=20&by-date=true
[22]: https://w14.monkrus.ws/search?q=Adobe+Animate&max-results=20&by-date=true
[23]: https://w14.monkrus.ws/search?q=Adobe+Character+Animator&max-results=20&by-date=true
[24]: https://w14.monkrus.ws/search?q=Adobe+Acrobat+Pro&max-results=20&by-date=true
[25]: https://w14.monkrus.ws/search?q=Adobe+Substance&max-results=20&by-date=true
[26]: https://w14.monkrus.ws/search?q=Adobe+Audition&max-results=20&by-date=true
[27]: https://w14.monkrus.ws/search?q=Adobe+XD&max-results=20&by-date=true
[28]: https://w14.monkrus.ws/search?q=Adobe+InDesign&max-results=20&by-date=true
[29]: https://w14.monkrus.ws/search?q=Adobe+Speech+to+Text&max-results=20&by-date=true
[30]: https://w14.monkrus.ws/search?q=Adobe+Master+Collection+2023&max-results=20&by-date=true
[31]: https://w14.monkrus.ws/search?q=Adobe+Media+Encoder&max-results=20&by-date=true
[32]: https://www.mediafire.com/file/jr0jqeynr4h21f9/Adobe_GenP_3.0.zip/file
[33]: https://www.mediafire.com/file/ipp9gj15xzty1uw/GenP_3.0_Release.zip/file
[34]: https://www.mediafire.com/file/re7hbvq8bbxmep1/Acropolis_V1.6.zip/file

<!-- Links End Main content Start -->

# Genp Method

> **~~[Video Tutorial: Updated Guide #2 - CC+GenP](https://odysee.com/@genp/guide2)~~ - Video outdated due to new versions of Genp, CCstopper and others**

## Downloads Needed

- 🔗 [Creative Cloud (CC)][11]
- 🔗 [GenP 3.0 - Modded][33]
- 🔗 [CCStopper][9]

!!!warning
[If you are having "Unlicensed popups | App will be disabled | Not loading or looping CC"](https://www.reddit.com/r/GenP/comments/ue47y6/possible_solution_to_unlicensed_app_popup_no/)
!!!

## Instructions

### 1. Download Genp 3 - Modded, CCStopper, and extract ALL contents from zip  
  **Antivirus may sometimes delete or move files into quarantine.**
  **You can either whitelist as safe or disable antivirus while extracting. This will fix the issue of **.exe** not showing in the folder after extracted.**

### 2. Download & Install Creative Cloud  
   - Create a free account or use one you already have, preferably without any ongoing subscription *(avoid problems)*
   - During setup, *if possible* do **NOT install AGS** (Adobe Genuine Service)
   - **Disable Auto-Update** on it's settings *if possible*.
   - Once that is done go `Menu > File > Exit Creative Cloud`

![](../static/genp-method/2-1.png)
![](../static/genp-method/2-2.png)
![](../static/genp-method/2-3.png)
![](../static/genp-method/2-4.png)

### 3. Using Powershell Commands to Patch Creative Cloud Desktop
***Thanks AbsentForeskin***

Restoring the "Install" buttons in Creative Cloud Desktop—in place of "Try" buttons, which demand payment information—is possible with PowerShell commands on the current most up-to-date version of Adobe Creative Cloud (v.5.11.0.521).  
Before you proceed, ensure this is the exact version specified next to "Apps" in the "About Creative Cloud" menu, as displayed below:
![](https://media.discordapp.net/attachments/971079960255164477/1122662145717440592/511-0-521.png)

Open an administrative PowerShell window to start and enter the following command to create a backup of your current Apps Panel: 

```
cp "C:\Program Files (x86)\Common Files\Adobe\Adobe Desktop Common\AppsPanel\AppsPanelBL.dll" "C:\Program Files (x86)\Common Files\Adobe\Adobe Desktop Common\AppsPanel\AppsPanelBL.dll.bak"
```

After creating the backup, apply the Apps Panel patch by pasting the entirety of the following code block into PowerShell:  
```
$bytes  = [System.IO.File]::ReadAllBytes("C:\Program Files (x86)\Common Files\Adobe\Adobe Desktop Common\AppsPanel\AppsPanelBL.dll")
$bytes[1117100] = 0xfe
$bytes[1216993] = 0xfe
$bytes[1988065] = 0xfe
$bytes[2149419] = 0xfe
$bytes[2150844] = 0xfe
$bytes[2151359] = 0xfe
$bytes[2152159] = 0xfe
$bytes[2278697] = 0xc6
$bytes[2278698] = 0x40
$bytes[2278707] = 0xc6
$bytes[2278708] = 0x40
$bytes[2278717] = 0xc6
$bytes[2278718] = 0x40
[System.IO.File]::WriteAllBytes("C:\Program Files (x86)\Common Files\Adobe\Adobe Desktop Common\AppsPanel\AppsPanelBL.dll", $bytes)
```
**NOTE:** If you receive an error stating that the file is being used by another process, use the command 
```
Stop-Process -Name "Adobe Desktop Service" -force
``` 
then re-enter the above code block.  

Reboot your machine after executing the code block to ensure Creative Cloud reinitializes fully. Upon startup, Creative Cloud will be patched and "Install" buttons will be present.  

If you've encountered an error and would like to restore from the backup, use the following command to do so:  
```
cp "C:\Program Files (x86)\Common Files\Adobe\Adobe Desktop Common\AppsPanel\AppsPanelBL.dll.bak" "C:\Program Files (x86)\Common Files\Adobe\Adobe Desktop Common\AppsPanel\AppsPanelBL.dll"
```

==- Old Method (Might not Work)
   - Go to the **default** folder for adobe in your file Explorer:  
   `C:\Program Files (x86)\Common Files\Adobe\Adobe Desktop Common\AppsPanel`  

   - Create a folder inside it named "BACKUP" and move the following files *(If you have them)* to it:  
    **AppsPanel.pimx, AppsPanelBL.dll and AppsPanellL.dll**  
    *(in case you want to restore them to default at a later date)*  

   - Go to `Genp 3 - Modded > Utilities > restore install buttons [beta]`, there will be another 2 "AppsPanel" files. You will copy these into the default AppsPanel folder (NOT THE BACKUP ONE).

![](../static/genp-method/3-1.png)
===

### 4. Use CCStopper to block ADS via Firewall (blocking internet)
   - **Run CCstopper as admin.** - You should be shown a menu with the following options which you must hit using the keyboard.  
   (2) for Internet Patch  
   (1) for Firewall Block.  

   Once that is done, you can select (Q) to quit CCStopper.

![](../static/genp-method/4-1.png)
![](../static/genp-method/4-2.png)

!!!
**PAY ATTENTION** - Firewall Rules should be in effect, therefore they won't let Creative Cloud load or Update *(this is intentional)*.  
⚠️ If antivirus is managing firewall settings, then you must create them in your antivirus firewall settings instead and not on windows *(whichever it is must be ON for the rules to take effect)* .
!!!

   - 💡Turn `Windows Firewall OFF`, then open Creative Cloud and wait for it to load, once its loaded then turn `Windows Firewall ON`
   - 🔁 **Repeat this process everytime you need to download other apps but get server error**  

(If you do not care for the explanation of this, you may skip to step 5)

==- ⚠️ Informational purpose only of step 4

*Explanation of what CCstopper does automatically with the use of the firewall rule*

Basically you are allowing internet access to Creative Cloud to load properly and blocking it again, by disabling and enabling the firewall rules.

Later you can disable, enable or delete them depending on your needs.
   * OUTBOUND: Stops information from leaving PC to the Server, helps bypass Credit Card prompt.
   * INBOUND: Stops information coming from Server to PC, helps bypass the trial countdown or app will be disabled prompt.

**How to add the same rules to firewall manually.**

- Go to `Windows Firewall > Advanced Settings`
- Create **Outbound** rules on the following:
   **Path of ADS** - `C:\Program Files (x86)\Common Files\Adobe\Adobe Desktop Common\ADS\Adobe Desktop Service.exe`
   **Path of Licensing** - `C:\ProgramFiles\Common Files\Adobe\Adobe Desktop Common\NGL\adobe_licensing_wf.exe`
   **Path of Licensing helper** - `C:\ProgramFiles\Common Files\Adobe\Adobe Desktop Common\NGL\adobe_licensing_wf_helper.exe`

**How to create it:**

   * **Rule type:** Program
   * **Program:** (Paste the directory above and select the application.exe)
   * **Action:** Block the connection
   * **Profile:** All
   * **Name:** (Choose a name that you will remember what it does)

The ADS rule is what causes Creative Cloud to take longer to load, not load at all or constantly loop, but its necessary to get in the app without triggering the CreditCard popup.

**Just remember that**

- Disabled: CreativeCloud works like normaly, but you cant download due to CreditCard popup.
- Enabled: The opposite happens, free to download but its stubborn a bit.

⚠️ **END of Informational purpose only of step 4**

===

### 5. Install Apps you want (Trial and Error)
=== For generative Fill
- Account must be set as higher than 18 years old
- You need to install photoshop beta for generative fill.
- To install photoshop beta, in CC go on `Apps > Categories > Beta Apps > Photoshop Beta`
===

   - If the buttons didn't get replaced with install, click on Try nonetheless and see if it starts downloading.  
   
   - Install all the apps you want in one go but don't open them yet. Wait until everything is installed, don't rush.

![](../static/genp-method/5-1.png)

### 6. Run GenP on the installed apps
   - Open `GenP folder > Resources > Run GenP file`

   - If you're having issues opening it, turn AntiVirus OFF and try again, however **don't forget to turn it back ON before selecting Try or Download**.

   - Click **"Search Files"** and wait. *(will look at the default locations, use custom path if installed somewhere else)*

   - You can de-select paths in case you have any versions you dont want to patch. (in case of using Monkrus Acrobat)

   - Finally click the **PILL** to run the patch.

!!!warning
OPEN THE APPS THROUGH THE .EXE and NOT FROM CC.
!!!

![](../static/genp-method/6-1.png)

### 7. Block Adobe Genuine Service URL
***Thanks S4M and AbsentForeskin***  
Launch PowerShell as administrator and enter the following
```
Add-Content -Path $env:windir\System32\drivers\etc\hosts -Value "`n0.0.0.0`tb5kbg2ggog.adobe.io" -Force
```
**Everything should be working now**

### 8. Optional - Block Each Installed app via Firewall  
   *(Case of issues like app will be disabled, day counter, unable to launch app due to some popup)*
   - Go to `Windows Firewall > Advanced Settings`  

   - Create **Inbound and Outbound** rule on each app with issues  
   **Typical path example would be:** `C:\Program Files\Adobe\Adobe Photoshop 2022\Photoshop.exe`  
   Find the proper path for the one you need.  

### 9. Optional - Block AGS via Firewall - *(similar to step 4)*
   -  Create both **Inbound** and **Outbound** rules on **Adobe Genuine Service**  
   Path of AGS - `C:\Program Files (x86)\Common Files\Adobe\Adobe Desktop Common\AdobeGenuineClient\AGSService.exe`

!!!
Always check first the monthly **[Compatibility List][5]** before updating any apps, otherwise don't update.  
If you want to install / update more apps, hit "**Install/Update**" on New app, let it download, and **run GenP** on them again.
!!!