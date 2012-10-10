This folder is for customized GUI XML files.

If you try to modify a file in the "cd_image/Gui/Default/" folder or one of it's childrens it will be automatically reverted by the patcher.

If you want to customize any of the GUI files you should first copy it to the "cd_image/Gui/Customized/" folder. If the file is located in a child folder of "cd_image/Gui/Default/" the same folder structure must be made in "cd_image/Gui/Customized/".

The game will first check the "cd_image/Gui/Customized/" folder to see if the file is there. If it is and the revision number is the same as the version in "cd_image/Gui/Default/", the customized version will be used. Any time the official version is updated the revision number will be increased. If the customized version have a different revision number than the official file, a warning dialog will be displayed ingame and the official file will be used.

If this happen you need to at least update the revision number in the customized file. But it is recommended to copy over the entire official file, and reapply the customizations you had done. This is to prevent you from loosing new functionality that might have been added to the file.

The revision number can also be used to temporarily prevent the game from loading a customized file. If it is set to '0' the official file will always be loaded and no warning dialog will pop up.


All GUI XML files start with a XML comment containing the revision number:

<!-- $Change: XXXXX $ (must be within the first 200 characters of the file) -->

Where XXXXX is the revision number.

