---
order: -3
---
# Blocking unnecessary Adobe Background processes (Photoshop/Acrobat DC)
*Thanks u/Verix- , from GenP Discord.*

## Photoshop

All you have to do is rename these 4 exe-files.

1. `C:\Program Files (x86)\Adobe\Adobe Sync\CoreSync\CoreSync.exe`
2. `C:\Program Files\Adobe\Adobe Creative Cloud Experience\CCXProcess.exe`
3. `C:\Program Files (x86)\Common Files\Adobe\Adobe Desktop Common\ADS\Adobe Desktop Service.exe`
4. `C:\Program Files\Common Files\Adobe\Creative Cloud Libraries\CCLibrary.exe`

Just add another letter after the ".exe".  
For example: "CoreSync.exe"-->"CoreSync.exeW"
(If you dont see ".exe" in the file name, you need to make the file name extensions visible in your explorer)

## Acrobat DC

All you have to do is rename these exe-file.

1. `C:\Program Files\Adobe\Acrobat DC\Acrobat\AdobeCollabSync.exe`

Just add another letter after the ".exe".  
For example: "AdobeCollabSync.exe"-->"AdobeCollabSync.exeV"  
(If you dont see ".exe" in the file name, you need to make the file name extensions visible in your explorer)

## For Updates on All

In order to update Creative Cloud, its recommended reverting at least the name change of `C:\Program Files (x86)\Common Files\Adobe\Adobe Desktop Common\ADS\Adobe Desktop Service.exe`.

To update the other apps, you should undo all changes to be on the safe side.