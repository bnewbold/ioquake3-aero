Advanced Enterprise Research Office
===================================

Advanced Enterprise Research Office is still in a somewhat hacked-together
state, so installing and running it require a bit of work.

It currently only runs on Mac OS X, due to a dependency on Quartz Composer. It
has been tested in Leopard (10.5.8).


Requirements
============
  
ioquake3
    http://ioquake3.org/get-it/
    Install it
  
the Quake 3: Arena CD-ROM
    Place the pak0.pk3 in your ioquake3/baseq3 folder
  
Quartz Composer
    Install instructions:
      http://quartzcomposer.com/quartz-composer-installation-tutorial-how-to-install
  
CamTwist
    http://allocinit.com/index.php?title=CamTwist
    Install it
  
Datamosh.plugin
    http://kriss.cx/tom/datamosh/
    Put it in:
      /Library/Graphics/Quartz Composer Plug-Ins/

aero.zip
    http://aero.electronicwhisper.com/
    Place the entire contents of this zip file in your ioquake3/baseq3 folder
      This includes RUN_AERO, the aero folder, and aeroquartz.qtz


Running
=======

Run RUN_AERO
    This will launch ioquake3 with the AERO mods
  
Press the ~ key
    This will give you back your mouse control
  
Move the ioquake3 window mostly off screen
  
Open CamTwist
    in "Video Sources" select "Desktop+", click "Select"
    in "Settings",
      uncheck "Full Screen"
      check "Confine to Application Window"
      select "ioquake3" from the list of windows
  
Run aero-quartz.qtz
    Make the viewer window big, ideally full-screening on your second monitor
  
Click on the ioquake3 window to focus it
  
Press the ~ key and you're off! Use the arrow keys to move around.

Hacking
=======

NOTE: Our working title for this mod was 'q3mosh' and despite some replace all
action you might still find that title floating around in path names etc.

All of our assets (including .map files, textures, music, etc) are in the
aero/pak*.pk3 file; these are simply zip files with a different file extension,
you can unzip them to get the original files.

Some game logic changes (eg new console commands) are bundled as compiled QVM
files. The actual source code changes relative to the ioquake3 source code
(relative to the 1772 subversion commit) are encapsulated in the
aero/ioquake3_aero.diff patch file.  We also have a git repository of the
source code changes at:

    http://github.com/bnewbold/ioquake3-aero

A few other changes (eg timescale) are implemented as simple command line
options (see RUN_AERO) or configuration flags (see autoexec.cfg in
aero/pak0.pk3)
