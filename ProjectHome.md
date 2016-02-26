## ge-satellite-tracker ##

A simple but powerful Python-Powered satellite tracker for Google Earth.

This is released using a no-strings-attached free software license.

Special thanks to [PICOL](http://www.picol.org/) for the current ground station icon and [IconShock](http://www.iconshock.com/) for the current satellite icon.

## how it works ##

First, follow the [installation instructions](http://code.google.com/p/ge-satellite-tracker/wiki/InstallationInstructions).  Once installed, using the satellite tracker is as simple as 1, 2, 3!

  1. Modify the getrack configuration file or just use the default
  1. Launch getrack by issuing 'python getrack.py'
  1. Drag and drop satellites.kml into Google Earth

## additional reading ##

  * [Inner Workings](http://code.google.com/p/ge-satellite-tracker/wiki/InnerWorkings)
  * [Blog: Satellite Tracker A First Look](http://libjoe.blogspot.com/2013/03/google-earth-satellite-tracker.html)
  * [Blog: Ground Station Update](http://libjoe.blogspot.com/2013/03/google-earth-satellite-tracker-update.html)
  * [Blog: Line of Sight Update](http://libjoe.blogspot.com/2013/03/google-earth-satellite-tracker-ground.html)
  * [Blog: Keps Caching Update](http://libjoe.blogspot.com/2013/03/google-earth-satellite-tracker-caching.html)
  * [Blog: Satellite Footprints Update](http://libjoe.blogspot.com/2013/03/google-earth-satellite-tracker_30.html)

## milestones ##

  * replace ugly template code with fastkml or simplekml
  * fix tear-drop footprints (caused by my lazy footprint code)
  * add fields of view to ground stations
  * add the concept of groups to ground stations where fields of view for grouped ground stations will be styled the same way, so you can view a ground station 'constellation' from afar
  * allow satellites to use unique icons
    * these will be stored in /icons
    * obtain unique satellite icons and associate them with the satellite names
  * consider supporting models in-place of icons (up in the air about this one)

### 03 April 2013 ###

  * cleaned up configuration defaults assignments
  * cleaned up server / port configuration items

### 30 March 2013 ###

  * added satellite footprints using a spherical earth model approximation
  * modified the configuration file logic (in favor of a config global)
  * if you like the defaults, you no longer need a config file

### 29 March 2013 ###

  * added support for caching keps, allowing for disconnected operation

### 26 March 2013 ###

  * added an option for dumping satellite names and improved the usage message

### 24 March 2013 ###

  * added line of sight functionality

### 23 March 2013 ###

  * added the ability to download keps from amsat (you can choose between amsat or spacetrack)
  * cleaned up most of the configuration globals
  * remove template txt files
  * cleaned up logging
  * added command line options and usage
  * added support for ground stations
  * fixed up some config sections code

### 16 March 2013 ###

  * initial commit!