OpenQuartz [![Status](https://travis-ci.org/jaredsburrows/OpenQuartz.svg?branch=master)](https://travis-ci.org/jaredsburrows/OpenQuartz)
=========

**Open Source Google Glass Development**

### Table of Contents  
 - [Getting Started](#getting-started)
   - [Official Examples](#getting-started)
   - [Important Libraries](#libraries)
   - [Important ADB Commands](#adb)
 - [Example Applications](#example-apps)  
   - OpenQuartz Open Source Applications
 - [Third Party Applications](#third-party)  
   - Useful third party applications
 - [External Links](#external-links)  
   - Official documentation and links for Google Glass as well as helpful links for developers 

<a name="getting-started"/>
### Google Glass Example GDK Applications:
 - [Compass](https://www.github.com/googleglass/apk-compass-sample)
 - [Level](https://www.github.com/googleglass/apk-level-sample)
 - [Stopwatch](https://www.github.com/googleglass/apk-stopwatch-sample)
 - [Waveform](https://www.github.com/googleglass/apk-waveform-sample)

<a name="libraries"/>
### Important Libraries:
 - Google
   - [Android Glass GDK](https://developers.google.com/glass/develop/gdk/)
   - [Android SDK](http://developer.android.com/sdk/index.html)
   - [Android NDK](Native Development Kit)(http://developer.android.com/tools/sdk/ndk/index.html)
 - Misc
   - [OpenCV(OpenCV for Android)](http://opencv.org/platforms/android.html)

<a name="adb"/>
### Basic ADB Usage(For Terminal or CMD Prompt):
Information for side loading Android applications.

 - Keep Your Google Glass On while charging/developing:
   - `adb shell svc power stayon true | false | usb | ac`
 - Turn off Wifi and only use Bluetooth
   - `adb shell svc wifi enable | disable`
 - Installing/Uninstall Applications(.apks):
   - `adb install -r FILE.apk`
   - `adb uninstall FILE.apk`
 - Running the Application:
   - `adb shell am start -n PACKAGE.NAME/.MAIN.ACTIVITY.NAME`
 - List all Packages on your Android Device:
   - `adb shell pm list packages -f` 
 - List all Relative Information about your Android Device:
   - `adb shell dumpsys`
     - `adb shell dumpsys battery`
     - `adb shell dumpsys wifi`
     - `adb shell dumpsys cpuinfo`
     - `adb shell dumpsys meminfo`
       - `adb shell dumpsys meminfo PACKAGE.NAME`
   - `adb shell cat "/system/build.prop" | grep "product"`
 - Screenshots from Commandline
   - `adb shell /system/bin/screencap -p /sdcard/screenshot.png`
   - `adb pull /sdcard/screenshot.png screenshot.png`

Read more: 
 - http://developer.android.com/tools/help/adb.html
 - http://stackoverflow.com/questions/11201659/whats-android-adb-shell-dumpsys-tool-and-its-benefits


<a name="example-apps"/>
### Example Applications for Google Glass:
 - GDK
   - [Camera App](GDK-CameraApp) - *Jared Burrows*
     - Basic Camera application with Camera preview - with "Hotfix" - post-XE11
   - [Memo App](GDK-GlassMemo) - *Andre Compagno*
     - Voice Memo Application
   - [Hello Glass](GDK-HelloGlass) - *Andre Compagno*
     - Basic "HelloWorld"
   - [Location Example](GDK-Location) - *Jared Burrows*
     - Basic Location on Live Cards
   - [Voice Example](GDK-VoiceExample) - *Andre Compagno*
     - Voice Recognition Example
 - OpenCV or Android SDK
   - [Glass Preview](SDK-CameraPreview) - *Jared Burrows*
     - "Hotfix" for Google Glass camera preview - post-XE11
   - [Image Manipulation](SDK-ImageManipulation) - *Jared Burrows*
     - Mixed Processing and Camera Control Tutorials
     - Canny, Sobel, RGBA, Gray, Feature Detection, etc
   - [Face Detection](SDK-FaceDetection) - *Jared Burrows*
     - "Hotfix" for Google Glass camera preview - post-XE11
     - Optimization coming soon


<a name="third-party"/>
### Third Party Applications([/third-party](third-party)):
Here are helpful applications to install on your Glass in order to start testing and developing.
- Android Applications
 - API Demos
 - Barcode Scanner
 - Capture Activity
 - Dev Tools
 - Launcher
   - Regular ICS Launcher
 - [Launchy (update to XE11 first)](https://github.com/kaze0/launchy)
 - [OpenCV for Android](https://play.google.com/store/apps/details?id=org.opencv.engine)
 - Settings(Settings.apk)
 - [Settings for Glass(Setttings_Full.apk)](http://forum.xda-developers.com/showthread.php?t=2576224)
 - [Terminal Emulator](https://play.google.com/store/apps/details?id=jackpal.androidterm)
- Helpful Tools
 - [Android Screen Monitor](https://code.google.com/p/android-screen-monitor/)

<a name="external-links"/>
### Google Glass Resources:
 - [Overview](https://developers.google.com/glass/)
 - [Basic Setup](https://glass.google.com/u/0/setup)
 - [Technical Specifications](https://support.google.com/glass/answer/3064128)
 - [Developer Guidelines](https://developers.google.com/glass/guidelines)
 - [GDK](https://developers.google.com/glass/develop/gdk/)
 - [Github](https://github.com/googleglass)
 - [Boot Images and Kernels](https://developers.google.com/glass/downloads/system)
 - [Glass-Apps: Developers, Blogs and News](http://glass-apps.org/)

<a name="license"/>
License
=========

    Copyright (C) 2015 OpenQuartz
   
    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
