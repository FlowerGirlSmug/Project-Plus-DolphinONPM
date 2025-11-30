# Ontario P+ Dolphin Troubleshooting

### *I highly recommend before your first netplay session to open Netplay Launcher.dol offline and let the shaders pre-compile ahead of time*

### This fork of Dolphin comes with 3 changes to the graphics settings that aim to reduce stutters
- "Compile Shaders Before Startup" is defaulted
- "Skip Drawing" shader compilation is defaulted
- A pre-made .uidcache file has been included for both Offline Launcher.dol and Netplay launcher.dol

When starting the game the first time you'll have to wait for Dolphin to fully compile the shaders, however it is worth it as it will **massiveley** deduce stutters, and then never has to be done again *(unless you change gfx backends)*! 
Even on lower end hardware my tests have shown at **MOST** compiling shaders could take 2 minutes, but most of your PC's will handle it much quicker.

.

### Help: My game shows a bright white screen or other really bad graphical glitches
This is what happens when "Skip Drawing" is used in combination with the .uidcache file, BUT without "Compile Shaders Before Startup" enabled. In order to fix this go to the user folder, which you can access by clicking File > Open User Folder in Dolphin. From here click the "Cache" folder and delete the "Shaders" folder. After deleting that folder refer to either workaround #1 or workaround #2 as seen below.

.

### Help: When attempting to pre-compile the shaders Dolphin crashes or something goes wrong
There are two workarounds for this

- Workaround #1: Simply turn off "Compile Shaders Before Startup" and load into the game again. This does mean you will be building the shader cache from scratch but thanks to Skip Drawing there shouldn't be any stutters, however there will be noticeable pop in and graphical glitches.
- Workaround #2: Switch "Skip Drawing" to "Specialized (Default)" in Graphics > General. From here boot into the game and play a few matches vs a CPU, in my tests 3-5 matches should be sufficient. After you can switch back to "Skip Drawing" and should be all set, however if graphical glitches still appear then go back to "Specialized (Default)" and keep playing more until "Skip Drawing" finally stops glitching out. Janky workaround i know....but hey it works ¯\_(ツ)_/¯
- **NOTE: You will have to do this for both Offline and Netplay.dol's as the cache is seperate for them.**
