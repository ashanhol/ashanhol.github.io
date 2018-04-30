---
layout: single
title:  "Android USB Port From Unity Error"
date:   2016-02-02 18:39:30 -0400 
#categories:  [ "Android", "Error", "Google Cardboard", "Unity", "Unity3D" ]
---

So I was trying to build my Google Cardboard app to an Android phone and I got this error.

![Error!??]({{site.url}}/assets/images/android_usb_port_unity_error/USB-issue.png)
<em style="display: block;">Error!??</em>

This error can happen any time you build an app to Android from Unity. I was confused because I had tried all different USB modes, made sure the Google Drivers (as well as the drivers for this particular model of phone) were all installed to the latest versions. I couldn’t possibly enable USB mode any more than I already did. I restarted my computer and Unity a whole bunch of times and every time it would stop on this screen.

![Trying to locate and Android device]({{site.url}}/assets/images/android_usb_port_unity_error/locateandroid.png)
<em style="display: block;">Trying to locate an Android device</em>

And give me that error above.

# How to fix it
Apparently developer mode wasn’t enabled. But I didn’t see a setting to turn on development tools like I thought there would be. I knew there was a way to do it, but finding it was very difficult if you didn’t know what you were looking for.

## Step 1. 
Go into your settings to where your Android version is listed. Should be somewhere in an “About phone” option.

![Android Build - About Phone]({{site.url}}/assets/images/android_usb_port_unity_error/androidbuild.png)
<em style="display: block;">Android Build - About Phone</em>

## Step 2. 
Tap the “Android version” until you see a dialogue box pop up at the bottom of the screen that says something along the lines of “Developer enables in *number* presses”. Tap that many more times and developer tools should be an option in your settings now. If you press it too many times you might see something like this.

![Android KitKat Screen]({{site.url}}/assets/images/android_usb_port_unity_error/androidkitkatscreen-e1454440597728.jpg)
<em style="display: block;">I swore I broke my phone</em>

I was extra confused since that isn’t the Android logo. Someone else pointed out it was a kitkat which is that build of Android.

Aaaanyways…

## Step 3. 
You should now see “Developer options” in your settings menu!

![Android Settings Menu - Developer Options]({{site.url}}/assets/images/android_usb_port_unity_error/developeroptions.png)
<em style="display: block">Android Settings Menu - Developer Options</em>
