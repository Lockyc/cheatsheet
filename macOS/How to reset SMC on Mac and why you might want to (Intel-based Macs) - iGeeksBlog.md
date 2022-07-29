---
created: 2022-07-29T13:27:17 (UTC +10:00)
tags: []
source: https://www.igeeksblog.com/how-to-reset-smc-on-mac/
author: Ankur
---

# How to reset SMC on Mac and why you might want to? (Intel-based Macs) - iGeeksBlog

> ## Excerpt
> Are things not working appropriately on your Mac? To reset SMC on Mac with the T2 chip: Click on the Apple logo > Shut Down your MacBook...

---
SMC stands for system management controller. When you face problems with your Mac and restarting does not solve it, you can reset the SMC. This can fix issues related to power, [thermal][1], fans, [charging][2], keyboard backlighting, battery, and more. The process depends on which type and model of Mac you have. Before learning how to reset SMC on any Mac, let us understand why you might want to do it.

**Note**: This guide is for Intel-based Macs. If you have an [M1 Mac][3], this is not applicable for you because SMC isn’t available on it.

![How to know if your Mac has Intel Processor or Apple Silicon](How%20to%20reset%20SMC%20on%20Mac%20and%20why%20you%20might%20want%20to%20(Intel-based%20Macs)%20-%20iGeeksBlog/how-to-know-if-your-mac-has-intel-processor-or-apple-silicon-1.jpg)

_To know if your Mac has an Intel processor or Apple chip, click the **Apple logo** at the top left and choose **About This Mac**._

## What is SMC responsible for on the Mac?

SMC takes care of several things, including actions that happen even when the Mac is off — for example, pressing the power button or the orange light when you connect the Mag Safe charger to your MacBook. Courtesy of official Apple Support, here is the list of actions SMC is responsible for.

-   Power, in the power button and USB ports.
-   Battery and charging.
-   Internal fans and other thermal-management features.
-   Indicators such as status indicator lights (sleep status, battery charging status, and others).
-   Sensors such as the sudden motion sensor, the ambient light sensor, and keyboard backlighting.
-   Behavior when opening and closing the lid of a MacBook.
-   Selecting an external (instead of internal) video source for some iMac displays.

## How to know that you need to reset Mac’s SMC

If you have problems related to any of the features mentioned above, resetting SMC will help. For example:

-   The keyboard backlight does not work correctly.
-   The light on the MagSafe charger does not behave properly.
-   Battery indicator lights (on the left side) on earlier MacBooks do not represent the right status.
-   Mac’s fan kicks in at full speeds even when there is no heavy use.
-   Screen brightness and keyboard backlight do not respond automatically to ambient light.
-   Mac’s power button is unresponsive.
-   You have issues while closing or opening the MacBook lid.
-   MacBook fails to charge.
-   Mac fails to recognize externally connected devices.
-   Random and unexpected shutdowns.
-   Unwarranted problems with target display mode.

If you face the problems mentioned above, resetting Mac’s SMC will help. Let’s check out how to do it.

-   [How to reset the SMC on your Mac][4]
    -   [Reset the SMC on MacBook with the T2 chip][5]
    -   [How to reset SMC on MacBook without the T2 chip][6]
-   [Reset SMC on Mac desktop computers with or without T2 chip][7]

## How to reset the SMC on your Mac

The steps are not the same for all Mac computers. Thus, it is essential to know about your Mac and follow the steps accordingly.

### Reset the SMC on MacBook with the T2 chip

Recent Mac desktops and notebooks (notably 2018 and later) have Apple T2 Security Chip responsible for encrypted storage, secure boot, enhanced image signal processing, and security for MacBook’s Touch ID data.

#### **Here is how to know if your Mac has the T2 chip or not.**

1.  Click the **Apple logo** → **About This Mac** → **System Report**.
2.  Select **Hardware** from the left sidebar and click **Controller**.
3.  If your Mac has the T2 chip, it will be mentioned here.![How to know if your Mac has T2 chip or not](How%20to%20reset%20SMC%20on%20Mac%20and%20why%20you%20might%20want%20to%20(Intel-based%20Macs)%20-%20iGeeksBlog/how-to-know-if-your-mac-has-t2-chip-or-not-1.jpg)

#### **Once you have identified that your MacBook has the T2 chip, here is how to reset the SMC.**

1.  Click the **Apple logo** and **Shut Down** your MacBook.
2.  On the in-built keyboard, press and hold **control + option + shift** for 7 seconds.  
    _**Important notes**: Press control and option from the keyboard’s left side and shift from the right side. (see image). It is okay if your MacBook turns on._
3.  After holding the above three keys for 7 seconds, press and hold the **power button** too. So now, you are pressing and holding a total of 4 keys.  
    _**Note:** Your Mac will turn off if it was on._
4.  Continue holding all the **four keys for 7 seconds** and then leave them.
5.  After a few seconds, press the **power button** to start your MacBook.![How to reset SMC on MacBook with T2 Chip](How%20to%20reset%20SMC%20on%20Mac%20and%20why%20you%20might%20want%20to%20(Intel-based%20Macs)%20-%20iGeeksBlog/how-to-reset-smc-on-macbook-with-t2-chip-1.jpg)

### How to reset SMC on MacBook without the T2 chip

If your MacBook does not have a T2 chip, the steps to reset SMC varies depending on what kind of battery it has – non-removable or removable battery.

-   **MacBook with non-removable battery**: MacBook Pro (mid-2009 through 2017), MacBook Air (2017 or earlier), other MacBook models except MacBook (13-inch, Mid 2009).
-   **MacBook with removable battery**: All MacBook models of early 2009 or earlier. Plus, MacBook (13-inch, Mid 2009).
-   _To know your MacBook’s year, click the **Apple logo** → **About This Mac**._

#### **Reset SMC on MacBook with a non-removable battery:**

1.  Click the Apple logo and **Shut Down** your MacBook.
2.  From the left side of the in-built keyboard, press and hold **shift + control + option**. (see image)
3.  Keep holding these three keys, and now also press and hold the **power button**.
4.  Continue holding all four keys for **10 seconds** and then leave them.
5.  Finally, press the **power button** to start your MacBook.![How to reset SMC on non T2 chip MacBook with non-removable battery](How%20to%20reset%20SMC%20on%20Mac%20and%20why%20you%20might%20want%20to%20(Intel-based%20Macs)%20-%20iGeeksBlog/how-to-reset-smc-on-non-t2-chip-macbook-with-non-removable-battery-1.jpg)

#### **Reset SMC on MacBook with a removable battery:**

1.  Click the Apple logo and **Shut Down** your MacBook.
2.  Carefully remove the internal battery. (See YouTube videos or take help from Apple Support, if needed.)
3.  Press and hold the **power button** for 5 seconds.
4.  Insert the battery again and press the power button to start the Mac.

### Reset SMC on Mac desktop computers with or without T2 chip

The process to reset SMC on iMac, iMac Pro, Mac Pro, Mac mini, etc., is the same.

1.  Click the Apple logo and choose **Shut Down**.
2.  Completely **unplug** the main power cord.
3.  Wait for **15 seconds** and **re-plug** the power cord.
4.  Wait for **5 seconds and press the power button** to start the Mac.

_**Note:**_ Since there is no confirmation popup or message, there is no concrete way to tell if the SMC reset was successful. However, if the problems mentioned earlier no longer exist, you can derive that it was successful.

A few people also suggested that after SMC reset, the time & date on your Mac may be slightly altered. The changed [energy saver][8] settings in System Preferences might also be restored to default.

I hope this guide helped you fix the issue, and now you have an improved Mac experience. If you have any questions, please reach me via the comments section.

**You will also find these helpful:**

-   [Wi-Fi Not Working on MacBook? How to Fix It][9]
-   [14 Ways to Speed Up a Slow Mac][10]
-   [macOS Big Sur Installation Failed? 10 Ways to Fix][11]
-   [How to Factory Reset any Mac][12]

[![](How%20to%20reset%20SMC%20on%20Mac%20and%20why%20you%20might%20want%20to%20(Intel-based%20Macs)%20-%20iGeeksBlog/97772c326e007a12ea9ac02b5c2e613d.png)][13]

I have been an Apple user for over seven years now. At iGeeksBlog, I love creating how-tos and troubleshooting guides that help people do more with their iPhone, iPad, Mac, AirPods, and Apple Watch. In my free time, I like to watch stand up comedy videos, tech documentaries, news debates, and political speeches.

[1]: https://www.igeeksblog.com/macbook-pro-overheating/
[2]: https://www.igeeksblog.com/macbook-not-charging/
[3]: https://www.igeeksblog.com/apple-m1-chip-faqs/
[4]: https://www.igeeksblog.com/how-to-reset-smc-on-mac/#reset-the-SMC
[5]: https://www.igeeksblog.com/how-to-reset-smc-on-mac/#T2-chip
[6]: https://www.igeeksblog.com/how-to-reset-smc-on-mac/#MacBook-without-T2-chip
[7]: https://www.igeeksblog.com/how-to-reset-smc-on-mac/#With-without-T2-Chip
[8]: https://www.igeeksblog.com/how-to-prevent-mac-from-sleeping/
[9]: https://www.igeeksblog.com/wifi-not-working-on-macbook/
[10]: https://www.igeeksblog.com/mac-running-slow/
[11]: https://www.igeeksblog.com/macos-big-sur-installation-failed/
[12]: https://www.igeeksblog.com/how-to-factory-reset-mac/
[13]: https://www.igeeksblog.com/author/ankur/
