# Quick Playblast
Quickly playblast things that were meant to playblasted...

The script allows you to hide your nurbs curves, everything but your geometry and nurbs surfaces and the resolution gate. You can also playblast your scene right from the same interface. I still need a Linux tester, so if you're reading this shoot me an email through my site or throw me a pm on here!

## What/Why:
I got tired of constantly having to hide everything during a playblast so I decided to write this quick script. The script allows you to hide your nurbs curves, grid, everything but the geometry and nurbs surfaces and resolution gate. It also allows you to playblast your scene straight from the script. It takes the height and width values from your render settings, but allows you to specify a percentage option so that it scales the playblast accordingly. The latest version adds quite a few more options:

- There's a tab specifically for modelers.
- There's now an option to "smooth" your selected geometry via a scroll list selection. (This was done by request)
- The code is also highly optimized now and should run much quicker than the older versions.

## Version Issues:
The only current issue is Linux playblast support. I don't have a Linux installation to test it out on, so I'm unsure of whether Linux has playblast support with sound now or not. I know this was an issue, so I will be adding in support via Grae Revell's script. His script can be found here:
http://www.creativecrash.com/maya/downloads/scripts-plugins/

## How To Install:

1) Put the enableQuickPlayblast.mel file into your scripts folder.
    - If you're using 2010 or lower, you do not need the .ui files.
    - If you're using 2011 and over, the .ui files are necessary.


2) Put the .bmp, .xpm or .iff file into your /prefs/icons folder (depending on your os and your Maya version):
    - OSX users will need the .iff file for 2010 and lower and the .bmp for 2011 and higher
    - Windows users can use the .bmp file for all versions)
    - The .xpm file should be universal for all platforms, however, I have had issues with .xpm on OSX in 2011 (it works fine on Windows though).

3) If you had a previously installed version (pre 2.9), go to your userSetup.mel file and remove the line:

    scriptJob -e "SceneOpened" "enableQuickPlayblast();" -per;

3a) Then simply change your shelf button command from this `quickPlayblast;` to `source enableQuickPlayblast.mel; quickPlayblast();`

3b) If this is your first time installing it put this script into your scripts folder and then put this into your shelf as a button: `source enableQuickPlayblast.mel; quickPlayblast();`

4) You can also choose an icon for it (if you wish) by going to your shelf editor and going to the shelf you've got it saved to. Then click on the quickPlayblast script you saved to the shelf remove the Icon name and click "Change Image..." (on Maya 2011 select the folder next to the Icon Name and remove the Icon Label). Grab the image from the icons directory you put them in and you're done!

## Notes:
The 2011 version is QT based, while the 2010 version is mel based. The 2010 version is equally as fantastic as the 2011 version!

## Quick Tips/Help:

### I don't know how to put something into my shelf. How do I do it?

Open Maya. Go to Window->General Editors->Script Editor. Make sure that the tab is set to Mel and type in the code. For this example we'll use the script for this particular script: source enableQuickPlayblast.mel; quickPlayblast();
Now select that entire text and in the script editor go to File-> Save Script to Shelf.

It'll ask you to name it. It's good to keep it short since the buttons can only handle about 4 letters (I use qPly). Then click ok. Alternatively, you can use a quick name for it and then replace that with the new icon in 2.9.2. That's it!


### How do I edit my shelf?

In Maya go to Window->Settings/Preferences->Shelf Editor. In 2011 it'll be a dual pane window so simply find the shelf you're using and click on it in the left hand side and then find the script you want to modify on the right hand side. In 2010 it'll be a tabbed display, so simply go to the shelves tab at the top, select the shelf you saved the script to and then go to the shelf contents. Find the script you want to modify by scrolling through the list and you're done.


### Why do I need to delete the 'scriptJob -e "SceneOpened" "enableQuickPlayblast();" -per;' line?

This script used to run as a script job when I first made it. I was experimenting with different options at the time and while it was an adequate solution at the time, it's not nearly as good a solution as it could have been.


### Where is the userSetup.mel file?

The userSetup.mel file is in the same location you should put the script in.

On Windows:
    Windows Vista and higher: C:\Users\username\Documents\maya\versionOfMaya\scripts (you may have My Documents instead of Documents if you upgraded from XP or just ported your stuff over, but it's the same directory)
    Windows XP and lower: C:\Documents and Settings\username\My Documents\maya\versionOfMaya\scripts

You can access this path via your My Documents folder rather than going through the whole hierarchy, but I put it there for completeness.

On OSX:
    /Users/username/Library/Preferences/Autodesk/maya/versionOfMaya/scripts


### Why do/don't I need the .ui files?

With Maya 2011 came the advent of the QT Interface. Maya 2010's interface is built off of mel. Maya 2011 went to a unified interface though, letting all platforms look the same and other neat stuff. QT's implementation has been wonderful (ramp shaders on OSX finally work!), even if some features are missing.


### I have my scripts split into sub-directories for cleanliness and your script doesn't work. Why?

You're probably using Maya 2011 and it can't find the .ui files. The reason this is, is Maya makes you hardcode the location of the .ui files into the script (or at least I haven't found a way to not have it hardcoded) so what you have to do is change one line in the file. Open the enableQuickPlayblast.mel file and go to line 49. It should read like this:

     string $quickPlayblastWindow =`loadUI -uiFile ($scriptsDirectory+"/quick_playblast.ui")`;

Simply put the directory of your folder in it like this:

     string $quickPlayblastWindow =`loadUI -uiFile ($scriptsDirectory+"/myDirectory/quick_playblast.ui")`;

and you'll be good to go.


## Testing:
Testing for this script is done on Maya 2010 and 2011-x64 on both OSX Snow Leopard and Windows 7 64 bit. If you spot a bug on a different version of Windows or OSX, please report it so I can make the changes. I can't test on every platform so help me help you.
