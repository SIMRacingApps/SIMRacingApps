# SIMRacingApps
## HTML5 Based Apps and Widgets, ReST Web Server and Java SDK
## A Companion to Your SIM Racing Games
=========================================================================================

## What is SIMRacingApps? 
  * It's a Web Server used to host Apps and Widgets, accessible using any device with a modern browser.
  * It comes with several Apps and Widgets free out of the box.
  * It's a ReST interface for developers to access the SIM Data via an HTTP call or using a WebSocket.
  * It's a HTML5 platform for other developers to write Apps and Widgets and share them with you.
  * It's a Java SDK for developing your own Java Based Apps that can work with any supported SIM.
  * It has a Plugin Interface for server side clients.
  * And it is free, open source, released under the Apache 2.0 license.
  * Like us on FaceBook [SIMRacingApps](https://www.facebook.com/SIMRacingApps) to keep up with new releases and tips and tricks.
  * Visit Our Web Page at [SIMRacingApps.com](https://SIMRacingApps.com) for more information.

## Here is a partial list of the Apps and Widgets that are included.
  * CrewChief (Control your pit changes. Calculate fuel mileage, laps on tires, etc.)
  * TrackMap  (See where all the cars are overlaid on Satellite or Street Map images)
  * Dashes    (with fully working analog and bar gauges like Tach, Water Temp, Oil Temp, etc.)
  * Standings (see pit time for all cars, best and last laps times, etc.)
  * Relative  (see who is near you)
  * RaceAdministrator (Makes those pesky admin commands a touch or click of the mouse)
  * Spectator/Broadcaster (Puts lots of information at your finger tips on one page with selectable driver)
  * And there are more. Install the server and access them from the main page.

## Want to try it out? It's simple. 
### On the same computer where the simulator is running:
  * Download the latest version of SIMRacingAppsServer....exe from the [releases page](https://www.github.com/SIMRacingApps/SIMRacingApps/releases/latest) and save it where you can find it later. It is not an installer, it is just an .exe file.
  * Execute SIMRacingAppsServer....exe. 
  * If you do not have Java 1.8 or better installed, it will direct you to the download page so you can install Java.
  * Leave the server window open while racing. You can minimize it, but note the HTTP://... address in the title of this window first. You will use the address to connect to the server from the clients.
  
### Clients can be from any device connected to your home network (including the SIM computer):
  * Open the browser (Chrome, FireFox, IE10, EDGE, Safari) and enter the HTTP address of the server.
  * Click on an App or Widget and start racing. Clicking the icon will get help for that App or Widget.
  * In addition to using browsers, I have provided packages for using the [Overwolf Apps](https://www.overwolf.com) and [Atom/Electron](https://github.com/atom/electron) platforms as clients for SIMRacingApps. Each platform has different features that might meet your specific needs. Refer to the readme provided with each package to get a better idea on which one would be best for you.
    
## There is more...

If you are a developer, you can develop your own Apps, Widgets or Plugins.
Detailed documentation is available right from the server's main page.
By making the source available, I hope others will join in and help develop this farther.
You can find the source on GitHub at https://www.github.com/SIMRacingApps. 
Just fork the source, make your changes and submit a pull request.

But, you do not have to be a GitHub expert to help out. 
You can simply develop your App or Widget in your personal folder and SIMRacingApps will scan for it and add it to the main page.
See below for details on creating your own App or Widget.
You can also share your App or Widget by creating a .SRA file that can be uploaded to the [FaceBook Group's](https://www.facebook.com/groups/SIMRacingApps) File Section. .SRA files are simply .ZIP files renamed that contain your App or Widget's files relative to the Documents/SIMRacingApps folder. The .SRA file is intended to be uploaded on the SIMRacingApps main menu at the bottom of the page. Each file in the archive will be extracted to the users personal folder located at Documents/SIMRacingApps.

## Developers: How to work with the SIMRacingApp's repositories
### [SIMRacingApps](https://github.com/SIMRacingApps/SIMRacingApps)

The SIMRacingApps repository is the main repository. 
It contains the Ant build file for creating the .exe and copying the docs to the website.

It does not contain any source code, but it will get tagged for releases and the .exe will can be found in the releases tab.

You don't need to download all the repositories to just work on one of them. 
Just fork the master branch, or one of the release branches and download the one you need.
Then, using the published SIMRacingAppsServer...exe, run it manually to override the classpath and put your copy first, as follows.

#### java -Xms256m -Xmx512m -classpath "{PathToYourCopyOfTheRepostoriesOutputFolder};{PathToSIMRacingAppsServerExe};{PathToUserDocumentsSIMRacingApps}" com.SIMRacingApps.Server

The output folder of each repository is a little different.
For more information, see the README.md files in each of the repositories.

Once you have committed your changes in your fork, send me a pull request and I will consider merging your changes into the master branch.

### [SIMRacingAppsServer](https://github.com/SIMRacingApps/SIMRacingAppsServer)

This repository contains the server side generic API interface implementation.
The structure of this repository is setup to support build a WAR file originally because I was going to deploy to TomCat. 
I found that Jetty worked better for my needs, as it had a way to create an embedded server as long as I started all the servlets myself. The final .exe that is built can also be used in the classpath for a Java based application just as you
would for a jar file.

### [SIMRacingAppsWebContent](https://github.com/SIMRacingApps/SIMRacingAppsWebContent)

This repository contains all the Web based Apps and Widgets.
It's has only 2 3rd party dependencies, RequireJS and AngularJS. 
Both are supplied in the repository. 
I do this so I do not rely on CDN providers and so it will load faster. 

### SIMRacingAppsSIMPlugin{SIM}

Each of the repositories that follow this naming convention is the implementation of a specific SIM's functionality.

The results of building this project may be used to include the SIM in the default .exe file that is created.
If not, the Ant build file can also build a .SRA file that can be uploaded to any SRA server installation to add a SIM manually.

1. [SIMRacingAppsSIMPluginTemplate](https://github.com/SIMRacingApps/SIMRacingAppsSIMPluginTemplate)
   This is a sample repository to use when starting a new SIM Plug-in.
1. [SIMRacingAppsSIMPluginiRacing](https://github.com/SIMRacingApps/SIMRacingAppsSIMPluginiRacing)
   This is a plug-in for https://iRacing.com.

### [SIMRacingAppsOverwolf](https://github.com/SIMRacingApps/SIMRacingAppsOverwolf)

Overwolf is 3rd Party Software that renders HTML5/JavaScript pages and injects them into the game's display.  

This repository is the main menu implemented as an Overwolf package.
It allows for launching Apps and Widgets and remembering the location and size of each.
It also allows for creating multiple configurations and switching between them.

NOTE: Due to Overwolf having issues from time to time with iRacing's anti-cheat software. 
I have become frustrated with trying to keep it working. As of the end of 2017, I am no longer actively supporting this. Feel free to clone this and work on it yourself and I will consider merging any pull requests you send me.

### [SIMRacingAppsElectron](https://github.com/SIMRacingApps/SIMRacingAppsElectron)

Electron is 3rd Party Software that renders HTML5/JavaScript pages in Native OS Windows.
It allows for control of how these windows look and feel.
The main menu is implemented in node.js code to create the windows and launch the Apps and Widgets within them.
It remember is the location and sizes of each window in a configuration. 
You can have multiple configurations as well as the ability to auto launch Apps and Widgets automatically.

NOTE: As of the 1.4 release of SIMRacingApps Server, the Electron client is bundled and enabled by default. 
If upgrading from an earlier version, it will not be enabled by default. 
To do so, add/update the following variables in the settings.

electron-autoupdate = Y

electron-autostart = Y


### [SIMRacingApps.github.io](https://github.com/SIMRacingApps/SIMRacingApps.github.io)

This repository is for the https://SIMRacingApps.com web site.
When pushing to this repository, GitHub automatically publishes the content to the web site.

The Ant build file in the [SIMRacingApps](https://github.com/SIMRacingApps/SIMRacingApps) repository
will automatically copy the documentation and version files to this repository.
So, any time you upload a new build, you should also commit and push this one as well. 

=========================================================================================

[Copyright (C) 2015 - 2019 Jeffrey Gilliam](https://SIMRacingApps.com/COPYRIGHT.TXT)

[Apache License 2.0](https://SIMRacingApps.com/LICENSE.TXT)
