# How to download and run an APK from MIT App Inventor on a Chromebook (without turning on Developer Mode)

## Step 0: Downloading the APK onto your Chromebook

Say you have an App Inventor APK, either created by you or someone else. This guide will go through how to run that APK on a Chromebook without having to turn on Developer Mode. 

After you download the APK file onto your Chromebook, if you try to open the APK, you may see the following message:

![Open MIT App Inventor](apk_screenshots/Step-0-2.png)

But don't worry! There is a way to sideload your APK onto your Chromebook through Linux without turning on Developer Mode.

## Step 1: Make sure you have Linux (Beta) installed and ADB enabled

These instructions are copied from Step 1 of the [ADB installation instructions](adb_on_chromebook.md):

We need to make sure you have Linux turned on with the right settings for Android development. Tap or click the bottom right corner of your Chromebook where it displays the time to pull up the options and settings menu.

There should be a gear icon that you can tap on to access the settings. Once you do so, the full Settings menu will be displayed in a window. 

In Settings, tap or click the three horizontal lines in the top left corner to bring up the expanded menu for Settings. A side menu should pop out from the left side of the window. You should see a penguin icon and **Linux (Beta)** near the bottom of the menu.

When you tap or click on **Linux (Beta)**, it should tell you if you have Linux enabled. In the screenshot below, it is enabled. If it's not enabled, you'll need to click "Turn On", and then "Install" it, which may take a few minutes.

Once you have made sure that Linux is installed and enabled on your Chromebook, you can tap or click the "Linux: Run Linux tools, editors, and IDEs on your Chromebook" box to see more settings. Once you've done that, you should see an expanded menu.

Tap or click on "Develop Android apps". This will show you whether or not ADB debugging is enabled. If the switch is gray/disabled, you'll need to enable it. This will trigger your Chromebook to restart. Once ADB debugging has been enabled, the switch should be on and blue.


## Step 2: Sideload your APK

After you've made sure that Linux is set up, you are ready to sideload your APK. First, open the Linux terminal. You can find the Linux terminal by tapping or swiping up from the bottom bar on your Chromebook and typing "Linux" in the Launcher. The terminal should open and look like this:

![Open MIT App Inventor](apk_screenshots/Step-3-0.png)

Type `adb connect 100.115.92.2:5555` into the terminal and press Enter to start the daemon. You want to see `connected to 100.115.92.2:5555` at the end:

![Open MIT App Inventor](apk_screenshots/Step-3-1.png)

Now, move your downloaded APK file from where it currently is into "Linux files". Here you can see the PIC.apk being dragged from the Downloads folder into "Linux files" in the sidebar:

![Open MIT App Inventor](apk_screenshots/Step-3-2.png)

Go back to the Linux terminal and type `adb install <YOUR APP NAME>.apk` to install your app. If you see an error telling you that you have more than one device, type `adb devices` to see the list. You can type `adb -s <DEVICE NAME> install <YOUR APP NAME>.apk` to select which device you want to install your app on. In the screenshot below, the PIC.apk was installed onto the Linux container at 100.115.92.2:5555

![Open MIT App Inventor](apk_screenshots/Step-3-3.png)

Now, you can find your app through the Launcher by scrolling down or typing your app name in the search bar:

![Open MIT App Inventor](apk_screenshots/Step-3-4.png)

You can tap or click your app to open it at any time.
