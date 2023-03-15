<p align="center">
    <img src="./src/oneuios.png"/>
  </p>

# Prerequire
To run it in Windows/MacOS/Linux, make sure you have ADB installed, if you didn't install, please click [me](https://developer.android.com/studio/releases/platform-tools) to install

Connect to your One UI device before running script
# What can this script do?
Debloat system apps to make your system to make your One UI faster, better battery life and improve privacy

⚠️Warning: This script debloat many system apps that can break some features, you can modify this script according to your need before running or reinstall apps using this command
~~~
adb shell cmd package install-existing <name of package>
~~~
For example, you want to restore Samsung Cloud, run this command:
~~~
adb shell cmd install-existing com.samsung.android.scloud  
~~~
# Run the script
Before running script, please download this repo and extract file, then go to folder One-UI-Optimization-Script
 Then, just run the script according to your OS. For running directly on android, please refer [this](#Termux)

# Windows
On Windows, right click on adbdebloat.bat and click Run as administator
or open Command prompt, head to the folder and run:
~~~
adbdebloat.bat
~~~
# MacOS/Linux
Right click on adbdebloat.sh and run
or open Terminal in this folder and run
~~~
bash adbdebloat.sh
~~~
or 
~~~
./adbdebloat.sh
~~~

# Termux
>Download Termux from [F-Droid](https://f-droid.org/en/packages/com.termux/) or [Github](https://github.com/termux/termux-app/releases), not Play Store

Make sure you granted storage permission for Termux:
~~~
termux-setup-storage
~~~

- For rooted devices:
 ~~~
 su
 ~~~
 ~~~
 cd /../../<your path to script>
~~~
Note: If your phone is rooted, you can use this [Debloater](https://github.com/sunilpaulmathew/De-Bloater) or Debloater Magisk Module instead of this method

- For non-root devices

To run directly on Android without PC, Android 11+ is required

First, setup Shizuku using Wireless Debugging
Now, Follow these step to using this debloater:

 Open Shizuku, select Use Shizuku in terminal apps, click export files, choose a folder and ok

 Use any text editor to replace PKG with com.termux in **rish** file

Note: Move termuxdebloat.sh to the same folder

 Now open Termux, execute the following commands
 ~~~
 cd /../.../<your folder>
~~~

For example, you stored it in Internal Storage/Termux. Just run this command

~~~
cd /storage/emulated/0/Termux
~~~

Run this command and grant Shizuku permission:
~~~
sh rish
~~~

Now, run **termuxdebloat.sh** and let it do everything for you
~~~
./termuxdebloat.sh
~~~
# After update
After update, system may reinstall some apps, just run script again.

Also after update, your device may be slower or drains battery so fast, run this command to optimize it:
~~~
adb shell cmd package bg-dexopt-job
~~~

On Termux, run this command

- For rooted devices
~~~
su -c "cmd package bg-dexopt-job"
~~~
 - For Termux+Shizuku, run this after **sh rish** command
 ~~~
 cmd package bg-dexopt-job
 ~~~

# Enjoy faster experience
<p align="center">
    <img src="./src/gaming.jpg"/>
  </p>

# Credit
- invinciblevenom for [One UI Debloat Script](https://github.com/invinciblevenom/debloat_samsung_android/blob/main/README.md)
- KelvinCrag for [Optimizer](https://github.com/KelvinCrag/Optimizer)
- Me
