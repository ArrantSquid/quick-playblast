2.9.2

- fixed a bug in 2008 where the buttons to toggle the different elements would not work. (Thanks again to Ty Viveiros for finding it)
- added an icon because I was tired of having to use the default one maya gives it (plus it looks nice).

2.9.1

- added the option for users to save the location of the playblast (Thanks to jarombrand for suggesting it)
- fixed a "bug" where the playblast window showed up during a playblast on Windows - Maya's playblast does the same thing on Windows, but I can't fix theirs. :) (Thanks to Ty Viveiros for pointing this out)
- removed the option to smooth individual geometry - it took up too much screen real estate. If you want it to look smooth then check the box and it smooths everything in the scene. If people really thought this was useful then let me know and I'll add it back. I find it useless. Good topology and then soften the normals. You've got a smooth mesh now and it's not done via Hotkey 3. Just MHO.


2.9
- fixed a bug with certain variables not saving their values correctly
- fixed a bug in maya 2011 for windows with playblasts being distorted (Thanks to Damien Hess for pointing it out)
- made the playblast filename default to the scene name
- added a button to hide everything but polygonal and nurbs surfaces
- added a button to change the background to a gradient
- made some ui improvements with interface elements specific to Mac OS or Windows
- minor code improvements
- moved the changelog to a separate file

2.8
- made some code improvements with the help of Eric E. Lenerville (http://eeltechart.com)
- updated the reset settings to work properly in Maya 2011
- made more layout changes
- made the script universal for maya 2010 and 2011, with a mel interface for 2010 and a qt interface for 2011

2.7
- fixed a display issue
- made line endings CRLF instead of LF for windows compatibility (even though most editors understand the difference)

2.6
- fixed an issue with the ui in 2011
- per the request of an animator there's now an option to select the geometry in your scene that you'd
like to have rendered as "smoothed" (aka hotkey 3).
- removed irrelevant functions

2.5
- rewrote script almost entirely from scratch - almost every function was redone entirely
- made the functions act only on the window that has focus
- made the functions so that they didn't disable options in the drop down menus
- increased response time of the script
- fixed an issue with no sound going with the playblasts - my apologies for the oversight
- enabled new options and toggles to better serve modelers
- redid the layout to make it clean enough that everything would fit (tabbed layouts are awesome)
- made an option on the modeling tab for choosing the compression type - it's still a playblast, but every bit helps (render at high resolutions so you can scale down. :)
- more nitty gritty codework that doesn't require anymore detail. :)

2.4
- added an option to reset the settings
- added a better about screen
- fixed initial variables
- changed variables and settings for functions

2.3
- recreated the layout to use maya 2011's new QT interface
- cleaned up the script and renamed some of the procedures and variables
- made better comments for the entire script

2.2
- fixed a bug in the way that the playblast rendered
- changed a variable name to not interfere with mayas own playblast options

2.1
- fixed a bug in the way OS X handles the resolution gate toggling
- added in comments for the code
- fixed a bug with how OS X handles menu bars with frame layouts.
- cleaned up the code and removed commented code (not comments, but code that had been commented)
- fixed the window size (since it was HUGE before)

2.0
- check for OS type now so we can output the correct file format!

1.5
- made playblast option integreated into it
- bugfixed erroneous code


1.0
- took code from hidemenurbs and ported it to this
- added in extra checks
- added in code for toggling
- added ui

