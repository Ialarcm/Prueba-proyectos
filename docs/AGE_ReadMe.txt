Advanced Genie Editor

This software is licensed using GNU General Public License Version 3 (GPLv3). This means that you are free to modify, (re)use, and (re)distribute the software as long as the license and copyright notices are preserved, and the full source code of your edition is made available. A copy of the GPLv3 license text can be found in the "AGE_License.txt" file in your distribution. The copyright notice for the software can be found in the source code.

For your convenience, a binary copy of the software is included with your distribution.

In accordance with the terms of GPLv3, the source code of this software is made available to you at the following location(s):
- "AGE_Source.zip" in your distribution

The latest version of this software is available at the following URL(s):
- https://github.com/Tapsa/AGE

Below is the ReadMe, Release Notes, and Credits for this software.

-------------------------------------------------------------

[b]Advanced Genie Editor[/b]
for Age of Empires, Rise of Rome, Age of Kings, The Conquerors (including HD), Star Wars Galactic Battlegrounds and Clone Campaigns.

This is a program for editing data of genie (DAT and DLL) files. It can edit properties of units, civilizations, technologies, graphics, terrains, sounds, player colors and some other things.

[b]Please[/b], ask questions on the [url=http://aok.heavengames.com/cgi-bin/forums/display.cgi?action=st&fn=9&tn=44059&st=recent&f=9,44059,0,365]forums[/url].

[color=blue]Check out [url=http://aok.heavengames.com/blacksmith/showfile.php?fileid=11349]this[/url] program also. It's for graphical modding.

For editing language files in The Conquerors,
I recommend [url=http://aok.heavengames.com/blacksmith/showfile.php?fileid=10819]this download[/url].[/color]

[b]Version History[/b]
Guide makers et cetera, please include the version into which your guide was written.

Version [b]2019.11.22[/b]:
-Fixed default paths for AoE II DE.

Version [b]2019.7.2[/b]:
-Negative armor types can be changed via effects.
-Supports newer game versions.

Version [b]2018.1.29[/b]:
-Marked resource multiplier as not available in AoE 1.

Version [b]2017.11.7[/b]:
-Internal unit name filter works the way it used to.
-Graphics can be filtered by rainbow.
-Images are saved centered on hotspot.

Version [b]2017.10.6[/b]:
-Saving an SLP handles player color properly.
-Deleting terrain tables uses correct indexes.
-Unit terrain table defaults to 0.
-Small improvements here and there.

Version [b]2017.5.17[/b]:
-Fixed loading order of DRS files.
-Fixed a problem with angle sound count.
-Editing box widths are customizable.
-New icon by gagman.

Version [b]2017.3.14[/b]:
-Scrolling lag fixed.
-Graphic sounds can be heard.
-Many unknowns named.
-Able to show loose SLP files along with DRS.
-Fixed bugs in saving data with enter.
-Can save as different game version.
-Fixed bugs in relisting.
-Improved tooltips all over.
-Fixed switching between building and unit icons.
-Pause between animations visible.
-SLP cache improved.

Version [b]2017.1.10[/b]:
-Fixed pasting terrains.
-Fixed buttons on terrain tables and borders.
-Mirrored graphics with two angles display properly.
-Added some helpful buttons to graphics tab.

Version [b]2016.12.30[/b]:
-Deltas with display angle should show properly.
-The actual terrain that is drawn is shown when selecting terrains.

Version [b]2016.12.23[/b]:
-Added WASD keys back to SLP view.
-SLP view can be zoomed.
-Fixed SLP view missing angles.
-Show angles dynamically shows exact angles.
-Better registry paths.

Version [b]2016.12.11[/b]:
-Fixed selection bug in armor combo box in effects.
-User interface fixes and improvements.

Version [b]2016.11.13[/b]:
-Fixed refreshing lists.

Version [b]2016.11.7[/b]:
-Removed broken batch editing from strings.

Version [b]2016.10.9[/b]:
-Reduced memory usage of combo boxes that share strings.

Version [b]2016.10.2[/b]:
-Reduced drawing lag.

[b]Notes[/b]

[color=BA0000]Make your own backups or use the auto-backup feature![/color]
Extract to anywhere and run.
You may need to run the program as administrator.
No help files are included.
No mod affects your already saved games, only new games.
You may be able to undo changes by going back to the text box and pressing Ctrl + Z.

[b]Tips[/b]

You can have multiple search entries separated with "|" letter.
Upper search boxes are inclusive and lower ones exclusive.
Example: "tower|ship|ram"
Use the check boxes to force match all entries.

[b]Developers[/b]

Mikko "Tapsa" P, since 2.0b
Apre - genieutils, 2.1a to 3.1
Estien Nifo aka StSB77, 1.0a to 2.0a

[b]Credits[/b]

Ykkrosh - GeniEd 1 source code
Scenario_t_c - GeniEd 2 source code
Alexandra "Taichi San", DarkRain654 - data file research
DiGiT, JustTesting1234, AOHH - genie file structure
Cysion, Kris, Sarthos - important help
BF_Tanks - some help
Donnieboy, Sarn, chab - tooltip texts
gagman - new icon

Follow coding [url=https://github.com/Tapsa/AGE/commits/master]here[/url] and [url=https://github.com/Tapsa/genieutils/commits/master]here[/url].

[url=http://aok.heavengames.com/blacksmith/lister.php?&pauthor=keisari%20tapsa&start=0&s=d&o=d]My other uploads[/url].

-------------------------------------------------------------

To compile you need to download MinGW, wxWidgets, Boost, and CMake.
I am using SFML for simultaneous audio playback.
Hopefully it will support MP3 in the year 2018.

CMake 3.15.5:
Install normally and select it to update PATH automatically.
You may need to edit version numbers in
\CMake\share\cmake-3.15\Modules\Find*.cmake
files to find wxWidgets and Boost.

Extract rest of the stuff into C:/Cpp or another folder which you like.

Mingw-builds 8.1.0: (includes gdb, libiconf, python, zlib)
Choose posix threads with dwarf exception handling.
After installing MinGW add its bin folder to the system path.

wxWidgets 3.1.3
Unpack the zip file.
In cmd.exe go to \wxWidgets\build\msw
mingw32-make -f makefile.gcc BUILD=debug clean
mingw32-make -f makefile.gcc BUILD=debug SHARED=1
mingw32-make -f makefile.gcc BUILD=release clean
mingw32-make -f makefile.gcc BUILD=release SHARED=1
del /s *.o
del /s *.o.d

Boost 1.71.0:
Unpack the zip file.
In cmd.exe go to \boost_1_71_0\tools\build
bootstrap.bat gcc
Copy b2.exe to \boost_1_71_0
Run from \boost_1_71_0
b2 toolset=gcc link=shared runtime-link=shared threading=multi install --with-iostreams
You can safely delete boost_1_71_0 folder after build completes.

SFML 2.5.1
Unpack the zip file.
Use the cmake-gui and browse the SFML source folder.
Configure and then generate both Release and Debug builds.
Run from \SFML mingw32-make install
Copy FindSFML.cmake to \CMake\share\cmake-3.15\Modules

You'll need to download Apre's DAT library from here:
https://github.com/Tapsa/genieutils
Then you'll need to download his DLL library:
https://github.com/Tapsa/pcrio
Place them into the same folder where AGE's folder is.
Update paths in build*.bat files, and then you are ready to go.

If building shared libs copy necessary DLL files to execution path or add lib paths to system path.
wx: base, core
Boost: iostreams
genieutils (after each change)