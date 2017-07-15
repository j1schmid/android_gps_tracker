# GPS based and gravity assisted geo tracker
The goal is to build a simple gps tracker for some sport activities for Android smart phones. Further the idea is to use the acceleration sensor data to estimate the track/route during when gps connection is lost. The sensor fusion might be handled using a "Kalman Filter".

The development notes and all refered ressources can be found in the source code or in some the [Markdown](https://en.wikipedia.org/wiki/Markdown) formated READMEs.

[Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

## Set up the android development environment
This short guid is based on the [fedoraproject wiki tutorial](https://fedoraproject.org/wiki/HOWTO_Setup_Android_Development) and is tested on a fedora 25 distribution.

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

su
mkdir /opt/android_sdk
unzip ..../downloads/android-studio-ide-162.4069837-linux.zip  -d /opt/android_sdk/


## further ressources

https://stackoverflow.com/questions/15670684/getting-gps-data-from-android-phone
https://stackoverflow.com/questions/1513485/how-do-i-get-the-current-gps-location-programmatically-in-android

Simple app to get and display the coordinates:
http://rdcworld-android.blogspot.ch/2012/01/get-current-location-coordinates-city.html 
