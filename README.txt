Introduction
============

 WerikUI is a partial replacement of the original Age of Conan: Hyborian Adventures
Graphical User Interface (GUI), specifically focusing on Player Portraits and the bottom Shortcutbars.
The main goal of this GUI modification is to provide a more minimalistic and informative look while
freeing up the space used by unneccessary visual elements.

Changes
============
Rev 49995 (2008/06/09) WerikUI v1.3.1

	FIX: A Simple Reversion number change to make it compatible
	     with the latest patch.

Rev 49054 (2008/06/03) WerikUI v1.3 - Current Version

	NEW: Redesigned group frame
	NEW: Three different layouts
		40x40 Icons for High Wide Screen Resolution
		32x32 Icons for High Wide Screen Resolution
		32x32 Icons for Non-Wide Screen Resolution with the player portraits
		      being moved a bit more to the center
	NEW: Matching colour for guild members in the Friend/Guild list
	NEW: The Slot Count of the shortcutbars was reduced to 10.
	     In exchange for the reduced slot count, the second half of the default Hotbar1 and Hotbar2 bars (Slot 11-20)
	     was were made into two extra separate shortcutbars with their own keybindings.
	     Use 1st & 2nd Extended Action Buttons from 11-20.


Rev 49054 (2008/05/29) WerikUI v1.2.2

	FIX: A Simple Reversion number change to make it compatible
	     with the latest patch.

Rev 48416 (2008/05/27) WerikUI v1.2.1

	FIX: A Simple Reversion number change to make it compatible
	     with the latest patch.

Rev 49054 (2008/05/21) WerikUI v1.2

	NEW: Added Target of Target to the Target Portrait.
	NEW: Added Latency bar to the bottom left corner of the screen.
	NEW: Added a tertiary, bindable ShortcutBar
             (Use the Left Action Button 1-6 options under Controls to bind keys to them)
	FIX: Reverted the ShortcutBar changes of the main bar to Multibar.
             Now you can shift between pages using the Action Page keys.
	FIX: Moved the Portraits a bit apart to better support the extra ShortcutBar.


Rev 49054 (2008/05/18 Early Access Client) WerikUI 1.1b

	FIX: Updated the revision numbers to match the latest patch


Rev 48901 (2008/05/17 Early Access Client)

	NEW: Redesigned the portrait frames. They should be more readable now.
	NEW: Replaced the target type text labels to icons.
	NEW: Removed the action list. It doesn't seem to serve a purpose,
	     I'm sure everyone can find the door without a flashing icon.
	FIX: The Hotbar frame backgrounds are corrected.
	FIX: Added Soul Fragment bar to the left of the player portrait frame.


Rev 48816 (2008/05/16) WerikUI 1.0

	NEW: Complete overhaul of the original AoC Shortcutbars. The shortcutbars are united into two 13 slot bars
	and the original multibar and it's alternate bar. You dont have to hold alt anymore to see the alternate bar.
	Most of the texture are stripped to free up space. The icon size is lowered.

	NEW: The player portraits are stripped from their background, the shape of the bars are changed to rectange
	from the original trapezoid shape.

	NEW: The Combat Rose is removed.

	NEW: Pet bar is removed.



	
Known Issues
============

Rev 49054 (2008/05/21) WerikUI v1.2

	- Holding the ALT key makes the main bar show MultiBar0, which is the same as the second ShortcutBar
	  Due to massive feedback and gameplay action bar shifting issues the benefit of this issue overweights
	  the above mentioned issue. As soon as I can find a way for disabling this feature of the Multibar it
	  will be fixed.



Rev 48816 (2008/05/16) WerikUI 1.0

	- Assassin's Soul Fragment bar isnt working yet. Sorry:/ Couldn't really figure it out how to handle it yet.
	- If there are more than one ActionList icon between the player and target portraits, they overlap the portraits.
	- The Extra Hotbar background frame is oversized.
	- The Lag Indicator is missing.
	- Cant shift between Shortcutbars.
	- The second button from the right can't be bound to any hotkey. I can't help this, this is most probably a bug
	  and it is reported.
	- And the rest I've not noticed yet :)




Installation Guideline

	1. Make a backup copy of your <Age of Conan>\cd_image\Gui\Customized\ folder if you are using other modifications.
	   They might be incompatible.
	2. Unpack the zip file in to a temporary directory.
	3. From the temporary directory, copy the _WHOLE_ cd_image directory into your <Age of Conan>\ folder.
	   (Yes, the whole cd_image directory, including both Customized and Default subdirectories)
	4.
	   a) If you use higher wide screen resolution and you want bigger icons,
	      rename cd_image_bigger_icons_for_widescreen to cd_image and copy it into your <Age of Conan>\ folder.
	      Choose YES for overwriting BottomBar.xml.
	   b) If you use smaller resolution and want to have more space for your chat windows, you can choose the version
	      where the player portraits are moved more into the center. To do so, rename
              cd_image_normal_closer_portrait and rename it to cd_image. Copy it into your <Age of Conan>\ folder.
	      Choose YES for overwriting BottomBar.xml.
	   

There are three pre-customized version of the UI:

 Normal version:		Uses the small 32x32 icon size
 Normal, portaits closer:	Uses the small 32x32 icon size and the player portraits are closer to the center
 Bigger icons for wide screen:	Uses 40x40 icon size (Recommended for high wide screen resolutions, 1920x1080 for example )


Directory Tree
============
	
<Age Of Conan Installation Directory>
 |_cd_image
   |_Gui
     |_Customized
     | |_Views
     |   |_HUD
     |
     |_Default
       |_gfx
         |_PortraitGUI
	   |_portraitsbottom

Revision Number changes (Out of Date Issues)
===========

Every time Funcom patches the game client the revision number increases.
This can cause that the modifications will be outdated and won't load anymore.
In this case you should get a warning during the launch of the game.

You can update the revision numbers yourself, though I'd not recommend it.
If the revision number of a file changes, there is a big chance that file was modified.
If you update the old file's revision number, you might loose new features which were 
introduced by the new patch.

Knowing this if you want to update your files, you must replace the revision number inside the XML files.
The XML files are always in cd_image\Gui\Customized\ .

Look for the the line:
	<!-- $Change: XXXXX $ (must be within the first 200 characters of the file) -->

where, XXXXX is the revision number. It is usually the second line of the file.

To find out what the correct revision number is, you have to check the exact same file inside
cd_image\Gui\Default. These are the default Age of Conan GUI layout files.

Example:

Lets say you want to change the revision number of your customized BottomBar.xml because at loading time the
game tells you that it's out of date.

In this case, you go to cd_image\Gui\Default\Views\HUD, open BottomBar.xml, and look at the second line.
The revision number is the number you can find between $Change: and the next $ sign.

Now you go to cd_image\Gui\Customized\Views\HUD, open BottomBar.xml, find the second line again, and replace the number
with the new revision number.
Save the file and you are good to go!


2008/05/16
Peter `weriK` Kovacs
kovpet@gmail.com






	 		      

