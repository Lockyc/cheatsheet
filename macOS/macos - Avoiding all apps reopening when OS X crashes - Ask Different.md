---
created: 2024-02-03T14:49:31 (UTC +10:00)
tags: []
source: https://apple.stackexchange.com/questions/129327/avoiding-all-apps-reopening-when-os-x-crashes
author: kettlepot
        
            1,7091111 gold badges3131 silver badges4242 bronze badges
---

# macos - Avoiding all apps reopening when OS X crashes - Ask Different

> ## Excerpt
> Sometimes my computer will crash and restart due to unknown errors. It usually happens when I'm working on something so a few apps are open. OS X has this annoying feature where it tries to reopen ...

---
# Permanently prevent macOS High Sierra from reopening apps after a restart

Works in macOS El Capitan, Yosemite, Sierra, High Sierra.

Solution: deny OS X access to the file it uses to store your session state. It prevents reopening apps even after reboot/shutdown from **Terminal**, from **AppleScript**, and system crash.

## GUI method

1.  Open Finder
2.  `Cmd+Shift+G` (Go to folder)
3.  Copypaste `~/Library/Preferences/ByHost/` and confirm
4.  Find the file starting with `com.apple.loginwindow`
5.  Doubleclick (opens in TextEdit)
6.  Remove all content and save the empty file. An additional confirmation dialog may appear.
7.  Right click, Get Info
8.  Lock the file (check the checkbox)

## GUI method (undo)

If you wish to undo this change later and re-enable the feature, simply delete this file and the OS will recreate it.

1.  Open Finder
2.  `Cmd+Shift+G` (Go to folder)
3.  Copypaste `~/Library/Preferences/ByHost/` and confirm
4.  Locate the file starting with `com.apple.loginwindow`
5.  Simply delete it

## CLI method

1.  Open Terminal.app
2.  Make the file owned by root (otherwise the OS will just replace it)
    
    ```
    sudo chown root ~/Library/Preferences/ByHost/com.apple.loginwindow*
    ```
    
3.  Remove all permissions, so it can't be read or written to
    
    ```
    sudo chmod 000 ~/Library/Preferences/ByHost/com.apple.loginwindow*
    ```
    

## CLI method (undo)

1.  Re-enable "reopen all apps" after login
    
    ```
    sudo rm -f ~/Library/Preferences/ByHost/com.apple.loginwindow*
    ```
