Random Configuration Settings
# Icon Bounce
source: https://git.herrbischoff.com/awesome-macos-command-line/about/
Global setting whether Dock icons should bounce when the respective application demands your attention.

## Enable (Default)
```
defaults write com.apple.dock no-bouncing -bool true && \
killall Dock
```

## Disable
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

# Software Update
## Set Software Update Check Interval
Set to check daily instead of weekly.
```
defaults write com.apple.SoftwareUpdate ScheduleFrequency -int 1
```
# Software Update
## Install All Available Software Updates
```
sudo softwareupdate -ia
```
## Show Available Software Updates
```
sudo softwareupdate --list
```
