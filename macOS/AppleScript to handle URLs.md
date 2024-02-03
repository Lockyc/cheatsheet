---
created: 2023-09-21T10:36:37 (UTC +10:00)
tags: []
source: https://gist.github.com/georgebrock/9ab3d83bf160b7c1c2b0
author: georgebrock
---

# AppleScript to handle URLs

> ## Excerpt
> AppleScript to handle URLs. GitHub Gist: instantly share code, notes, and snippets.

---
Follow these instructions to create an AppleScript App that can be used to open URLs, e.g. from [Choosy](https://www.choosyosx.com).

1. Open Script Editor (in `/Applications/Utilities`).
2. Write a script with an `on open location` handler (see `example.applescript`).
3. Save the script as an application (select "Application" from the file format dropdown in the save dialog in Script Editor).
4. Edit the application's `Info.plist` file to add a `CFBundleURLTypes` section, indicating it can handle HTTP URLs (see `Info.plist`). If the app is at `~/Applications/MyApp.app` then the `Info.plist` will be at `~/Applications/MyApp.app/Contents/Info.plist`.
5. Test your application from the command line using `open -a ~/Applications/MyApp.app http://www.example.com`
6. Update the AppleScript to do something useful with the URL (the [`do shell script` command](http://www.cyberciti.biz/faq/mac-osx-applescript-run-shell-script/) might be useful if you want to avoid writing more AppleScript).
7. ?
8. Profit.

## example.applescript
```applescript
on open location this_URL
	display alert this_URL
end open location
```