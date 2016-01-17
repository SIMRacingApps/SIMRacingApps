# SIMRacingApps
## HTML5 Based Apps and Widgets, ReST Web Server and Java SDK
## A Companion to Your SIM Racing Games
=========================================================================================

## What is SIMRacingApps? 
  * It's a Web Server used to host Apps and Widgets, accessible using any device with a modern browser.
  * It comes with several Apps and Widgets free out of the box.
  * It's a ReST interface for developers to access the SIM Data via an HTTP call.
  * It's a HTML5 platform for other developers to write Apps and Widgets and share them with you.
  * It's a Java SDK for developing your own Java Based Apps that can work with any supported SIM.
  * It has a Plugin Interface for server side clients.
  * And it is free, open source, released under the Apache 2.0 license.
  * Like us on facebook [SIMRacingApps](http://www.facebook.com/SIMRacingApps) to keep up with new releases and tips and tricks.
  * Visit Our Web Page at [SIMRacingApps.com](http://SIMRacingApps.com) for more information.

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
  * Download the latest version of SIMRacingAppsServer....exe from the [releases page](http://www.github.com/SIMRacingApps/SIMRacingApps/releases/latest) and save it where you can find it later. It is not an installer.
  * Execute SIMRacingAppsServer....exe. 
  * If you do not have Java 1.8 or better installed, it will direct you to the download page so you can install Java.
  * Leave the server window open while racing. You can minimize it, but note the HTTP://... address in the title of this window first. You will use the address to connect to the server from the clients.
  
### Clients can be from any device connected to your home network (including the SIM computer):
  * Open the browser (Chrome, FireFox, IE10, EDGE, Safari) and enter the HTTP address of the server.
  * Click on an App or Widget and start racing. Clicking the icon will get help for that App or Widget.
  * In addition to using browsers, I have provided packages for using the [Overwolf Apps](http://www.overwolf.com) and [Atom/Electron](https://github.com/atom/electron) platforms as clients for SIMRacingApps. Each platform has different features that might meet your specific needs. Refer to the readme provided with each package to get a better idea on which one would be best for you.
    
## There is more...

If you are a developer, you can develop your own Apps, Widgets or Plugins.
Detailed documentation is available right from the server's main page.
By making the source available, I hope others will join in and help develop this farther. 
Just fork the source, make your changes and submit a pull request.

But, you do not have to be a Github expert to help out. 
You can simply develop your App or Widget in your personal folder and SIMRacingApps will scan for it and add it to the main page.
See below for details on creating your own App or Widget.
You can also share your App or Widget by creating a .SRA file that can be uploaded from the main page using the form at the bottom of the page. .SRA files are simply .ZIP files renamed. They are intended to be uploaded on the main menu. Each file in the archive will be extracted to the users personal folder located at Documents/SIMRacingApps.

## How to work with the SIMRacingApp's repositories
### SIMRacingAppsServer

TBD

### SIMRacingAppsSIMPlugin{SIM}

TBD

=========================================================================================

[Copyright (C) 2015 - 2016 Jeffrey Gilliam](http://SIMRacingApps.com/COPYRIGHT.TXT)

[Apache License 2.0](http://SIMRacingApps.com/LICENSE.TXT)
