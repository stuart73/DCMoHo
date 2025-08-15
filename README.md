A working build of Moho for the PC running Windows 10/11
=================================================

You will still need to install Moho from the original CD as this repository does not contain any of the game resource files.

IMPORTANT. When installing Moho from the original CD, install it somewhere your local user account has 'write' access to. (i.e. NOT Program Files X86).  This is because game saves are stored in the installation folder.

This repository is a fork off LemonHaze420 repository which contained the original Moho source code for PC/Dreamcast and PlayStation year 2000

This fork fixes issues that prevent this game from running on modern hardware as well as adding new features.

Changes include:-

-Fixes code bugs that prevented the original code from building and running.

-Option for the game to be played in a window.

-Re-enabled the Level Editor, which was included in the original code but never released in the 2000 build.

-Removed checks for Moho needing to be installed.

-Removed any need for the original CD to inserted. It can now play FMVs and Music from the installed folder rather than just from the CD. 

I will provide a prebuilt .exe in the 'releases' part on this repository.

To build the replacement Moho.exe:-
==============================
-Download the code and files from this repository.

-Install Visual Studio community (I used 2022).  Make sure the options for C++ development and Windows SDK are installed as well.

-Start Visual studio and select the 'ballz.sln' file as the solution to open.

-Select 'Release' as the build output and select 'Build solution'

-Replace the Moho.exe with the newly one created in visual studio. 


Note: it is possible to run/debug Moho from Visual Studio, but requires you copying the binkw32.dll from the installed Moho location to your project location i.e. where the source code is.

Moho requires Bink header files/libs and also some directx7 input lib.  I've already provided these in the project.

Optional for FMV and music to run without a CD:-
========================================
-Copy the contents of 'data/video' from the CD into the installed Moho folder.

-Music is a bit trickier and requires you first ripping the CD like a normal music CD.  This can be done with the default 'Windows media player' 'rip music' feature. IMPORTANT: set the output format as '.WAV Lossless'.  You can then copy the output wav files to 'data/Music' on your installed Moho location. The track names may be wrong when ripping and need to be renamed to simply Track01 to Track05.

i.e. it should look like this:
Moho\Data\Music

    Track01.wav
    
    Track02.wav
    
    Track03.wav
    
    Track04.wav
    
    Track05.wav
    

-If you wish to use the level editor, make sure you copy the files in the data\Editor data from this repository to your installed Moho location.

To play
======
You can then run and play Moho. I recommend running the game in windowed mode at 1280x1024 resolution.

There is a level editor in the game, but be warned, this was an in-house tool and never expected to be released. Expect user-unfriendliness and bugs.

To access the level editor, select 'F6' when in game on any level.  I will leave notes about keyboard buttons for the editor in data\Editor\EditorNotes.txt file.  I'm not an expert on how to use this editor.

Known issues
===========
-FMV and the front end run at 640x480 no matter what resolution you select.   However in game works ok.

-Seems to say 'Exit game' rather than 'Moho' in the start screen.

-Not sure the correct music is played when playing music from the installation folder rather than the CD.
