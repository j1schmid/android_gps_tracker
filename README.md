# GPS based and gravity assisted geo tracker
The goal is to build a simple gps tracker for some sport activities for Android smart phones. Further the idea is to use the acceleration sensor data to estimate the track/route during when gps connection is lost. The sensor fusion might be handled using a "Kalman Filter".

The development notes and all refered ressources can be found in the source code or in some the [Markdown](https://en.wikipedia.org/wiki/Markdown) formated READMEs.

... [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
... [Markdown Wiki](https://en.wikipedia.org/wiki/Markdown)
... [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

## Set up the android development environment
### Configure device
#### Samsung Galaxy S4 mini
Settings -> More -> About device, tap a cuple of times onto the buld number, now the developement mode should be enabled. Now above About device Developer mode should appear, enable USB debugging. Connect the device to the computer and run ```adb devices``` now the device should appear on the list.

### Android Studio [IN PROGRESS]

Installation according to [Android Studio on Fedora 26](https://cialu.net/install-android-studio-fedora-26/), some additional information can be retrieved from the [official Android Studio installation guide](https://developer.android.com/studio/install.html).

Download [Anrdoid Studio IDE](https://developer.android.com/studio/index.html) and install the required tools and libraries:
```
dnf install zlib.i686 ncurses-libs.i686 bzip2-libs.i686
dnf install libgcc.i686

[MIGHT NOT NECESSARY] dnf install compat-libstdc++-296.i686 compat-libstdc++-33.i686 compat-libstdc++-33.x86_64 glibc.i686 glibc-devel.i686 libstdc++.i686 libX11-devel.i686 libXrender.i686 libXrandr.i686
```
Unpack and install Android Studio:
```
unzip ~/Downloads/android-studio-ide-version-linux.zip -d /opt/
cd /opt/android-studio/bin/
./studio.sh
```


### Eclipse IDE [IN PROGRESS]
This short guid is based on the [fedoraproject wiki tutorial](https://fedoraproject.org/wiki/HOWTO_Setup_Android_Development) and is tested on a fedora 25 distribution.

```
dnf install eclipse-jdt
download SDK (Software Development Kit) https://developer.android.com/studio/index.html
start eclipse, workspace e.g.: workspace/gps_gravity_app/eclipse_workspace

help -> About Eclipse Platform
	Version: Neon.3 (4.6.3)
	Build id: X20170404-1016
help -> install new software
	Available Software Sites 
		Add
			Name: e.g. Eclipse Update
			Location: http://download.eclipse.org/releases/neon/
		Add
			Name: e.g. Android Plugin
			Location: https://dl-ssl.google.com/android/eclipse/
		Reload
	Work with: Android Plugin -> Choose Developer Tools -> Next ....
restart eclipse
```

Install andorid SDK (software development kit):
```
download sdk from https://developer.android.com/studio/index.html
su
mkdir /opt/android_sdk
unzip ..../downloads/android-studio-ide-162.4069837-linux.zip  -d /opt/android_sdk/


cd /opt/android_sdk
./tools/bin/sdkmanager --list
./tools/bin/sdkmanager --update
./tools/bin/sdkmanager platform-tools "platforms;android-17" "platforms;android-8" "sources;android-17" "build-tools;26.0.0"
```


```
download sdk tools for linux:
wget https://dl.google.com/android/repository/sdk-tools-linux-3859397.zip ~/downloads

```

HTC Desire HD: ??? Andorid 2.2 ???, API level 8
Samsung Galaxy S4 mini: Andoid 4.2.2, API level 17

[Andoid Version List (German)](https://de.wikipedia.org/wiki/Liste_von_Android-Versionen)
[Andoid Version List (English)](https://en.wikipedia.org/wiki/Android_version_history)
[](https://developer.android.com/studio/command-line/index.html)
[](https://developer.android.com/studio/command-line/sdkmanager.html)

## further ressources

https://stackoverflow.com/questions/15670684/getting-gps-data-from-android-phone
https://stackoverflow.com/questions/1513485/how-do-i-get-the-current-gps-location-programmatically-in-android

Simple app to get and display the coordinates: [Read out and displays the GPS data](http://rdcworld-android.blogspot.ch/2012/01/get-current-location-coordinates-city.html)
