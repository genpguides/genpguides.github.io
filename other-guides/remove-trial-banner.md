---
order: -2
---
# Remove "Trial Expires in XX Days" / "Trial Ended" / "Trial Popup" Banner
*Thanks u/songmj36 and Lian (GenP Discord)*

!!!info
THIS IS ONLY AESTHETIC! IF THE PATCH WORKS, AFTER TRIAL ENDS THE APP CONTINUES TO WORK. Don't lose your head because its counting down or says it ended.
!!!

## 1. Remove "Trial Expires in XX Days" Banner

1. Edit *(as admin)* the file located in
    - **For Photoshop and others:** `Program Files\Common Files\Adobe\UXP\extensions\com.adobe.ccx.start\css\styles.css`
    - **For Illustrator:** `Program Files\Adobe\Adobe Illustrator 20XX\Support Files\Required\UXP\extensions\com.adobe.ccx.start\css\styles.css`
        - For **4.3.0** search for {*"background-color":"#1473E6"*} replace with {**"display":"none"**}
        - For **4.2.0 or below**: search for {*background-color:#1473E6*} replace with {**display:none**}  

**ATTENTION: Color code has changed NEW -> background-color:#D7373F**

## 2. Remove "Trial Ended" Banner

2. Edit *(as admin)* the file located in
    - **For Photoshop and others:** `Program Files\Common Files\Adobe\UXP\extensions\com.adobe.ccx.start\css\styles.css`
    > According to Louis, in Discord, (Thanks)  
    > After a certain update on Photoshop, the location of the "css" becomes the same path as Illustrator, but for Adobe Photoshop 20XX.

    - **For Illustrator:** `Program Files\Adobe\Adobe Illustrator 20XX\Support Files\Required\UXP\extensions\com.adobe.ccx.start\css\styles.css`
        - For **4.3.0** search for {*"background-color":"#e34859"*} replace with {**"display":"none"**}
        - For **4.2.0 or below**: search for {*background-color:#e34859*} replace with {**display:none**}

**ATTENTION: Color code has changed NEW -> background-color:#D7373F**

## 3. Remove Trial Popup: *(example: No UXP folder found)*
*Thanks u/narcarsiss*

This is for Adobe 2020, but may work with other installs.

**Confirmed working for InDesign, Photoshop and Dreamweaver!**

1. Navigate to: `C:\Program Files (x86)\Common Files\Adobe\AdobeGCClient\locales`  
**Remove your Language for me I removed:**  
example: "en-US.pak" and "en-GB.pak"   

**No more trial popup :icon-smiley:**
