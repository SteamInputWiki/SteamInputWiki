# Chapter 03b: Bindings Overview

This chapter will go over the various things that you can bind to buttons in a bit more depth.

## Mouse Buttons

* Left/Right Click
* Scroll Up/Down
* Middle Click
* Mouse Button 4 and 5
* Mouse Delta Binding - the 4 arrows at the bottom middle of the graphics for the Mouse
  * This allows you to set up a button that nudges the mouse cursor in a direction by an amount.
  * When you select this Binding, a dialog box appears that allows you to configure which direction and by how much, via an x axis slider and a y axis slider
  * On the x axis slider, negative numbers move the mouse cursor to the left and positive numbers move it to the right.
  * On the y axis slider, positive numbers move it DOWN while negative numbers move it UP

## Keyboard Buttons

These are pretty much “what you see is what you get”.

Unfortunate absences include:

* F13-24 keys
* Fn, or “Function” key
* please add to this list if you can think of any

## Gamepad Buttons

NOTE: If you are using a non-xbox controller, these are NOT available to the Desktop configuration.

These are Xinput - or XBox - commands. When using them, the game will think you are using a XBox Controller. This means you will get xbox controller prompts/glyphs in game. Exception; if the developer is tieing into the Steam Input API just enough to query Steam for which controller is being used. Developers, full SIAPI implementation is NOT needed to do this so please do.

* When Binding the Triggers, full value will be sent to the game
* You CAN Bind joystick directions by selecting the edge of the joystick direction you want to bind
  * However, this will also send full value to the game
* You bind the Joystick Clicks by selecting the CENTER of the joysticks

## SIAPI In-Game Actions

If the game has implemented SIAPI, that game will have predefined Bindings, called Actions, for you to assign. Instead of seeing any of the mouse, keyboard, or gamepad buttons, you will instead see a grid of these predefined Bindings. What these Actions are varies by game.

## Steam/Steam Input/System Bindings

These Bindings interact with Steam, Steam Input, or your PC. The list below is done from left to right.

* Action Set or Action Layer Binding - 3 stacked circles with looping arrows
  * Only visible if the configuration has more than 1 Action Set or has any Action Layers.
  * Action Sets and Layers will be covered in more detail in chapter 04.
* Show Keyboard - it looks like a keyboard
  * This opens Steam’s On Screen Keyboard.
* Take Screenshot - looks like a camera
  * This triggers Steam’s screenshot, taking a photo of what is on your screen and adding it to your Steam screenshot library
* Move Cursor - looks like a mouse cursor with circles around the tip
  * Unlike the Mouse Delta binding, this binding moves the cursor to a specific place on screen
* Toggle Magnifier - looks like a magnifying glass
  * This binding opens your computers on screen Magnifier for accessibility.
* Power Options - looks like a power button symbol
  * This binding has several different functions. Upon selecting, a dialog box with a drop down menu opens so you can select the desired function
  * Turn off Controller - this function immediately powers down your controller.
  * Exit Application - force quits the game, or whatever program is focused on your desktop
  * Open Big Picture - launches Steam’s Big Picture Mode
  * Minimize Big Picture - minimizes Steam’s Big Picture Mode
  * Quit Big Picture - exits Steam’s Big Picture Mode
  * Suspend Host PC - Steam Link function: puts the host pc to sleep
  * Shutdown Host PC - Steam Link function: turns the host pc off
  * Restart Host PC - Steam Link function: restarts host pc
  * Touchscreen Hover - ???
  * Touchscreen Left Click - ???
  * Touchscreen Right Click - ???
  * Touchscreen Middle Click - ???
  * Touchscreen Native - ???
* Set Light Options - looks like a light bulb
  * This binding allows you to customize lighting on your controller.
  * It opens a dialog box with a drop down menu and two sliders
  * The dropdown menu selects between 3 behaviours: Default User Setting (set in the General Controller settings), Default XInput Slot Number Setting (visual indicator of your player number when using xbox controllers), and Custom Setting (this bindings sliders).
  * The Controller Light Color slider selects which color you would like the lighting in your controller to change to. NOTE: Only works with controllers that have RGB lighting
  * The Controller Light Saturation slider determines how bright the light is.
* Steam Music Bindings - looks like a musical note
  * This binding interacts with Steam’s Music Player, giving you access to its controls. The dialog box that opens on selecting the binding allows you to choose which control you would like. The available controls are:
  * Play/Pause, Next, Previous, Volume Up, Volume Down, Mute
* The EMPTY Binding - looks like a circle with a horizontal line in the middle
  * This Binding literally does nothing.
  * It is used when you want a button to do nothing while an Action Layer is applied. Simply removing the Binding does not work, due to limitations of Steam Input.
* Change Controller Player Number - looks like a controller with two circles with people in them above it
  * In a local multiplayer game, this binding allows you to select which player you are instead of passing controllers around. The dialog box allows you to select player number 1-16.
