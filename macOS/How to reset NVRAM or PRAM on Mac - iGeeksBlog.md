---
created: 2022-07-29T13:27:11 (UTC +10:00)
tags: []
source: https://www.igeeksblog.com/reset-nvram-or-pram-on-mac/
author: Ankur
---

# How to reset NVRAM or PRAM on Mac - iGeeksBlog

> ## Excerpt
> How to reset NVRAM or PRAM on all Mac models: Click Apple logo > Choose Shut Down > Turn on Mac > Press and hold option + command ⌘ + P + R keys together...

---
Is your beloved Apple device, Mac acting… weird? If you are facing trouble booting it or its volume, mouse scroll, or display settings are all messed up, you may need to do more than restarting it. You may need to reset NVRAM or PRAM on Mac to fix the issue!

NVRAM (_non-volatile random-access memory_) on Intel-based Macs and PRAM (_Parameter RAM_) on old PowerPC are responsible for storing your Mac’s settings. Chances are they may have gone haywire.

Let me tell you more about each and show you how to reset NVRAM or PRAM to fix specific Mac problems.

**Note**: If you own a Mac [with Apple Silicon][1], the following guide does not apply to you.

## What is the work of NVRAM and PRAM on Mac?

NVRAM and PRAM are small, always-powered memory that holds Mac’s configuration information like the startup disk, screen resolution, time zone, volume, and more.

There is a small battery in Mac desktops to prevent the loss of these essential pieces of information. This ensures that even if you switch off or remove the main power cord on your iMac, things work correctly. On Mac notebooks (MacBook Air and MacBook Pro), there is already a battery inside.

## Why and when should you reset the NVRAM or PRAM?

If you have problems related to the settings controlled by NVRAM or PRAM (and if a simple restart does not help), resetting NVRAM or PRAM will solve the issue. This includes:

-   Different disk boot-up than the one set in Startup Disk preferences.
-   A question mark when you power on your Mac.
-   Increase in Mac’s shutdown time.
-   Lagging issues (the legendary rainbow spinning wheel doesn’t show up).
-   Incorrect clock or time zone.
-   Problem with the sound output or volume levels.
-   Erratic mouse scroll and click speed.
-   Changing display resolution on every startup (or no changes at all).
-   AirPort issues.
-   Hard drives or external displays don’t connect.

## How to reset NVRAM or PRAM on Intel-based Macs

1.  Click the **Apple logo** at the top left and choose **Shut Down**.
2.  Once done, turn on your Mac and immediately press and hold **option + command ⌘ + P + R** keys together for around 20 secs.  
    ![Press and hold Option Command P and R keys to reset NVRAM or PRAM on Mac](How%20to%20reset%20NVRAM%20or%20PRAM%20on%20Mac%20-%20iGeeksBlog/press-and-hold-option-command-p-and-r-keys-to-reset-nvram-or-pram-on-mac.jpg)
3.  During this time, you will notice that Mac appears to restart.
4.  You have to leave the keys **after your Mac boots twice**. That is:  
    \> On older Macs, leave the four keys when you hear the second startup chime.  
    \> On newer [Macs with T2 Security Chip][2] that do not make a startup sound, leave the four keys after the Apple logo appears and disappears for the second time.

This is how you can reset NVRAM or PRAM on your Mac. After this is done and your Mac powers on, you might notice different settings like time, time zone, volume, etc.

To change these, click the **Apple logo** and choose **System Preferences**. Next, click the appropriate options (or use the search box) and set them accordingly.

**Important notes:**

-   If your Mac has a firmware password, you cannot reset NVRAM or PRAM. [Turn off the firmware password][3] and then follow the above steps.
-   If your Mac computer (not MacBook) resets these basic settings (time, volume, etc.) after shut down, this means the small battery (we talked about above) needs replacement. If you have the technical know-how, you can take the help of online video tutorials to change the battery. They are inexpensive. Or contact an authorized Apple service center. At times, unauthorized shops may charge a considerable amount for this small replacement.

## FAQs

**Q. What happens when you reset the PRAM on Mac?**

Your Mac will restore its default hardware settings upon resetting your Mac’s PRAM or NVRAM. To do so, press option + command ⌘ + P + R keys together for around 20 secs (until you hear the second startup chime) after shutting down your system.

**Q. How do you know if your PRAM is reset?**

On older Macs, you will hear the second startup chime when your PRAM has been reset. Whereas, on newer Macs with T2 Security Chip, the Apple logo will appear and disappear for the second time. Thus, signaling that the PRAM has been reset.

**Q. How do I check NVRAM on Mac?**

To check NVRAM’s comprehensive contents and status, go to Terminal (Application > Utilities), type **nvram -xp**, press Enter.

**More Mac-related posts for you:**

-   [How to reset SMC on Mac and why you might want to? (Intel-based Macs)][4]
-   [How to disable Safari tab previews on Mac][5]
-   [Methods to listen to Audible on Mac][6]
-   [Mind mapping software for Mac][7]

[![iGB app](How%20to%20reset%20NVRAM%20or%20PRAM%20on%20Mac%20-%20iGeeksBlog/700-X-315.jpg)][8]  
_iGeeksBlog has affiliate and sponsored partnerships. We may earn commissions on purchases made using our links. However, this doesn’t affect the recommendations our writers make. You can read more about our [review and editorial process here.][9]_

[![](How%20to%20reset%20NVRAM%20or%20PRAM%20on%20Mac%20-%20iGeeksBlog/97772c326e007a12ea9ac02b5c2e613d.png)][10]

I have been an Apple user for over seven years now. At iGeeksBlog, I love creating how-tos and troubleshooting guides that help people do more with their iPhone, iPad, Mac, AirPods, and Apple Watch. In my free time, I like to watch stand up comedy videos, tech documentaries, news debates, and political speeches.

[1]: https://www.igeeksblog.com/apple-m1-chip-faqs/
[2]: https://www.igeeksblog.com/how-to-reset-smc-on-mac/#T2-chip
[3]: https://support.apple.com/en-us/HT204455
[4]: https://www.igeeksblog.com/how-to-reset-smc-on-mac/
[5]: https://www.igeeksblog.com/disable-safari-tab-previews-on-mac/
[6]: https://www.igeeksblog.com/how-to-listen-to-audible-on-mac/
[7]: https://www.igeeksblog.com/best-mind-mapping-software-for-mac/
[8]: https://apps.apple.com/app/igeeksblog-tech-news-tips/id1567408764
[9]: https://www.igeeksblog.com/review-editorial-guidelines/
[10]: https://www.igeeksblog.com/author/ankur/
