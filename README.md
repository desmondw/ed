ed - The ComputerCraft IDE
===
Last edit before repo: 9/25/12

This program was written for ComputerCraft 1.4 and likely will not function properly on the most recent version of ComputerCraft.

Background
---
From the moment I started using ComputerCraft I found many functions of the mod quirky and maybe a little frustrating, but the native editting program (edit) was unacceptable. Even for a monochrome text program with no mouse support and limited visibility there was still massive areas needing improvement. So I mostly coded in Notepad++ while I learned lua and the CC apis. Until I realized I need a new project and I know enough now to write MY OWN edit program. So, here it is.

Installation
---
To install, turn on http use in your ComputerCraft config file and use the pastebin command (i.e. pastebin get D1S03niy ed).

### v0.3
Direct: http://pastebin.com/D1S03niy

Adfly: http://adf.ly/D7lKX

### v0.2.1
Direct: http://pastebin.com/1fezqbQf

Adfly: http://adf.ly/D9Qcl

Features
---
* In-editor program execution, with debugger
* Customizable interface including line numbers and status bar that is saved across sessions
* Many improvements to movement controls and automatic text insertion
* One button saving, exiting, and running
* Support for turtles and terminals with custom screen sizes
* ...and more to come!

How to Use
---
Just like the native edit program, it runs with a single paramater, the file you wish to edit. In example, "ed myFile" without quotations.

Controls:
* F1 - Menu
* F3 - Save
* F4 - Exit
* F5 - Run
* F6 - Run with arguments
* F12 - Help

Planned Features
---
* *Movement hotkeys such as Ctrl+Home/End/arrows
* *Hotkey to duplicate lines
* *Selecting text
* **Copying text
* An auto-save / file-recovery feature
* Auto-updater
* Find and replace
* Goto line
* Auto-complete
* Printer support
* ~~Quitting without saving handling, and pressing quit button again to override~~
* ~~An options menu to change visual and functional preferences~~
* ~~Running the program being edited without exiting the IDE~~
* ~~Minor debugging features~~
* ~~Page Up and Page Down support~~
* ~~Insertion/overlay toggle for typing~~
* ~~Auto tabbing~~

_*These features may or may not require detecting multiple keys pressed at once, and therefore depend on ComputerCraft's ability to recognize multiple key presses at once._

_**Dependent on Minecraft's and ComputerCraft's ability to support it._




Screenshots
---
![alt tag](/screenshots/editor.jpg)
![alt tag](/screenshots/help.jpg)
![alt tag](/screenshots/options.jpg)
![alt tag](/screenshots/debugger.jpg)

Changelog
---
### v0.3 - 9/25/12
This feels like a big update to me, because a couple major goals were reached, and ed is officially over 1,000 lines of code! Woo!

Disclaimer:
Until I can think of a good way to represent menus in the turtle's screen, consider ed to be terminal-only support.
You can still do most things on turtles, but menu text will run off screen and you won't be able to see what settings you are changing.
However you are still able to edit the settings manually by opening up the settings file after going into the settings menu once to generate the file.

Changes:
* Added insertion/overwrite toggle
* Added status bar (optional) with the following information (which is all optional):
	* Current line number
	* Total line count (off by default)
	* Insert/overwrite toggle display
* Added debugging. The file no longer needs to be force-saved to run it, and if there are any run-time errors ed will move the cursor to the error line and display the error.
* You can now run ed from ed as recursively as you'd like and everything should work properly (yo dawg!)
* Added auto-tabbing
* Trying to edit files in non-existant directories now creates those directories
* Added settings menu, you can finally customize the UI without editing the code!.
	* Press F1 to access it, then use the arrow keys and space/enter to interact.
* Settings will automatically save on menu exit and load with the program - change it once and you're good! Settings are saved to ".ed_settings" and will overwrite all files and directories (sorry!)
* Added help screen (F12) that shows users the controls. By default "F12 = help" is shown in the status bar so no one is left wondering how to save, exit, etc, their first time.

### v0.2.1 - 9/23/12
This is a very minor update to fix a visual bug with the new version, CC 1.42, which will now be the solely supported version.
I tried to allow exiting the running programs by pressing F4, but it's not feasible to do without user-assistance (which doesn't really seem worth it).
If you want to exit a running program, you can still use Ctrl+T if your program allows it, and it will return cleanly to the IDE.
And in case you didn't know, pasting is already natively supported by the system, so it works in this IDE. The only reason it doesn't work in edit is because they have a Ctrl toggled menu.

* Now compatible with and supporting CC 1.42 (may not work with previous versions)
* Added message shown when file is saving
* Now resets program settings after program execution
* Now able to run programs with arguments, press F6 to do so
	* Note that running the IDE from itself will not exit cleanly at the momnent; see http://www.computercraft.info/forums2/index.php?/topic/4336-brunning-false-but-still-running/

### v0.2 - 9/22/12
I'm glad to have finally gotten to some of the more fun stuff, which is part of what is listed below. Also it should be noted that there's a lot of customizability already available if you're willing to poke around in the variables at the top of the code. I won't be adding the settings in-program until I've made a menu system of some sort.

Changes:
* Refactored and simplified code to reduce possible errors
* Added message display at the bottom for general information (e.g. program saved, program execution success/failure)
* Added exit without saving confirmation
* Added in-editor program execution (F5)
* Added tab support (more annoying to implement than you'd think...)
* Added page up and page down support
* Changed exit code to return true if exiting normally or false if due to an error

### v0.1 - 9/20/12
There's a LOT still to do, so far I think I've written a program comparable to edit. This initial post is just to get the program out there, since I've already had people steal the code on CC servers. It is not guaranteed to be bug free; if there are any bugs please let me know.

Features added:
* Line display on left side
* One-button saving and exitting
