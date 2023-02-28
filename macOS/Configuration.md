Random Configuration Settings
# Icon Bounce
source: https://git.herrbischoff.com/awesome-macos-command-line/about/

Global setting whether Dock icons should bounce when the respective application demands your attention.

## Disable bouncing
```
defaults write com.apple.dock no-bouncing -bool true && \
killall Dock
```

## Enable bouncing (Default)
or delete the key?
```
defaults write com.apple.dock no-bouncing -bool false && \
killall Dock
```

# Expand Save Panel by Default
source: https://git.herrbischoff.com/awesome-macos-command-line/about/
```
defaults write -g NSNavPanelExpandedStateForSaveMode -bool true && \
defaults write -g NSNavPanelExpandedStateForSaveMode2 -bool true
```
# Usability hack: Click & drag anywhere in macOS windows to move them
source: https://www.mackungfu.org/UsabilityhackClickdraganywhereinmacOSwindowstomovethem

Restart inbetween, or restart specific app for it to work for that app

From now on you can hold down Ctrl+Cmd, then click and drag ANYWHERE in a window to move it.

## Enable
```
defaults write -g NSWindowShouldDragOnGesture -bool true
```

## Disable
```
defaults delete -g NSWindowShouldDragOnGesture
```


# Software Update
## Set Software Update Check Interval
Set to check daily instead of weekly.
```
defaults write com.apple.SoftwareUpdate ScheduleFrequency -int 1
```
## Install All Available Software Updates
```
sudo softwareupdate -ia
```
## Show Available Software Updates
```
sudo softwareupdate --list
```

# Turn off low power mode
![CleanShot 2023-02-28 at 14 29 03@2x](https://user-images.githubusercontent.com/1438799/221754240-fb2220a0-828b-43d5-9859-c28e78a4912b.png)

