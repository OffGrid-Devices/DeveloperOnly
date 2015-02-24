# DeveloperOnly — GUIDELINES

This repository only contains this README file and is intended for Qathan developers only. It provides guidelines on how to develop and distribute Qathan devices for MaxForLive.  

## Instructions for developing Qathan Devices

1. The *master branch* is used for distribution only, so it only contains the Ableton Live pack installer for our users to easily install the Qathan device (often containing *Lessons*, *Samples*, *Clips*, *Presets*, etc...);

2. The *development branch* contains all files used in the development process, so it would normally contain a final/working version;

3. In order to make changes to the development files you should pull from the *development branch* to a new branch and give it a name like *UI-improvements*, for example;

4. To clone a Qathan device project to your computer go to the desired repository and click the *Clone in Desktop* button. Then save the repository to "~/Documents/Max/Max for Live Devices/QathanDevices/". All file dependencies should be stored in the created repository folder in a [max package format](https://cycling74.com/sdk/MaxSDK-6.1.3/html/chapter_appendix_f.html)

5. The *README* file of the *development branch* has a changelog that should be update whenever changes are made. Besides, you should also increment the [version number](http://semver.org/) of the Qathan device when updating changes. Basically, given a version number MAJOR.MINOR.PATCH, increment the:
...* MAJOR version when you make incompatible API changes,
...* MINOR version when you add functionality in a backwards-compatible manner, and
...* PATCH version when you make backwards-compatible bug fixes.

6. Whenever a stable release is accomplished you should make a *github release* in order to keep a backup of all versions of the device. When making a *release* from the *development branch* name it as (for example) "Q.device-dev v.1.1.5". When making a release from the *master branch* name it as (for example) "Q.device-pack v.1.1.5" or just "Q.device v.1.1.5". Remember that *master* branches contain an Ableton Live Package file (.alp) and *development* branches contain all development Max files (such as abstractions, externals, etc.) in a Max Package format.

7. In order to make it easier to develop Qathan devices in collaboration the patch structure should be as follows:
..* main patch: contains all user interface objects (if possible, because some will have to go onto bpatchers);
..* all other objects in the main patch should be *abstractions* and not *patchers* so that it is possible to have more than one person working on the same device as well as to improve maintainability.
 

## Instructions for distributing Qathan Devices

1. When saving the max for live device don't forget to *freeze* the device before saving it.
[Why?](https://cycling74.com/docs/max6/dynamic/c74_docs.html#live_sharing);
2. To make a *Live Pack* go to Ableton Live window, then *View > File Manager > Manage Project > Create Pack*;
3. Afterwards pull the project file (.alp) to the *master* branch 

## Licensing

1. [Choose a CC licence](https://creativecommons.org/choose/) 
2. Apply it to the *README* file of both the *master* and *development* branches.
