---
created: 2022-11-01T11:35:14 (UTC +10:00)
tags: []
source: https://support.apple.com/en-us/HT202528
author: 
---

# Turn on performance mode for macOS Server - Apple Support

> ## Excerpt
> Performance mode changes the system parameters of your Mac. These changes take better advantage of your hardware for demanding server applications.

---
Performance mode changes the system parameters of your Mac. These changes take better advantage of your hardware for demanding server applications.

If you need to run high-performance services on a Mac with macOS Server, you can turn on performance mode to dedicate additional system resources for server applications.

## OS X El Capitan 10.11 and later

To turn on performance mode in OS X El Capitan 10.11 and later, use the `nvram` command to adjust the _boot-args_ NVRAM variable. If you [reset NVRAM][1], this setting is cleared.

This command displays the _boot-args_ NVRAM variable. If you see _serverperfmode=1_, performance mode is already turned on.

```
nvram boot-args

```

If performance mode isn't already turned on, you can enable it by setting _serverperfmode=1_ in the _boot-args_ NVRAM variable with this command:

```
sudo nvram boot-args="serverperfmode=1 $(nvram boot-args 2>/dev/null | cut -f 2-)"

```

To turn off performance mode, use this command:

```
sudo nvram boot-args="$(nvram boot-args 2>/dev/null | sed -e $'s/boot-args\t//;s/serverperfmode=1//')"

```

![](Turn%20on%20performance%20mode%20for%20macOS%20Server%20-%20Apple%20Support/divider.png) 

## Earlier versions of macOS

To turn on performance mode in OS X Mountain Lion, OS X Mavericks, or OS X Yosemite, use the serverinfo command in Terminal.

To get the current mode, use the command:

```
serverinfo --perfmode

```

To turn on performance mode:

```
serverinfo --setperfmode 1

```

To turn off performance mode:

```
serverinfo --setperfmode 0

```

Transitioning to or from performance mode requires a restart.

![](Turn%20on%20performance%20mode%20for%20macOS%20Server%20-%20Apple%20Support/divider.png) 

## Learn more

If you're a developer, and want to learn more about how performance mode can optimize your system for server-specific applications, see the [sysctl(3) manual page][2].

Published Date: May 04, 2022

[1]: https://support.apple.com/kb/HT204063
[2]: https://developer.apple.com/library/archive/documentation/System/Conceptual/ManPages_iPhoneOS/man3/sysctl.3.html
