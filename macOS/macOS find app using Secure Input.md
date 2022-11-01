---
created: 2022-10-27T14:15:34 (UTC +10:00)
tags: []
source: https://rakhesh.com/mac/macos-find-app-using-secure-input/
author: 
---

# macOS: find app using Secure Input – rakhesh.com

> ## Excerpt
> Blog

---
Ran into an irritating problem today with my task switcher Contexts. It stopped working and there was an orange exclamation mark in the menu bar saying some application has Secure Input turned on and until I close it Contexts can’t work. Initially it told me that Firefox was responsible, and I was about to close it when I realized that whenever I switch to a different app it blames that app as having Secure Input turned on. 

So clearly the issue is elsewhere. [This page](https://smilesoftware.com/textexpander/secureinput/?) gives you a list of apps that can usually have Secure Input turned on. Thanks to [this forum post](https://forum.keyboardmaestro.com/t/disable-secure-input/2410/4) I learnt that you can find the offending app by running the following command:

```ioreg -l -w 0 | grep SecureInput```

Find the process ID from the `kCGSSessionSecureInputPID` field. Then use a activity monitor (easier, you can sort) or the following command:

```ps auxww | grep &lt;pid&gt;```

In my case the culprit turned out to be `loginwindow`. I tried to kill it but the system warned me that it would log me out. I was in no mood to get logged out, so upon a whim I tried locking and unlocking the system. That worked! :)
