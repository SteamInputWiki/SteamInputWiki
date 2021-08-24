# Chapter 2b - Section 9: Touch Menu

Touch menus are the original method to create lots of virtual buttons out of a smaller
number of physical inputs. Originally designed to be used via touchpads, this input style
now supports the gyro and dpads as well.

*[ Sora's note: it works on a dpad, strictly speaking, but it's moderately awkward to use
and doesn't feel good to me. If you're looking for something like this on a dpad, I'd
recommend trying the Hotbar Menu style. ]*

This style works by providing a grid of buttons on-screen for you to select and activate.
If you would prefer a circular style of multiple buttons (like how a weapon wheel works),
or if you want to use a joystick (which does not support touch menus), try the Radial Menu
style.

This on-screen display requires the Steam Big Picture Mode Overlay to be functioning and
available. If the overlay can't be used with your game, or the overlay is the regular
desktop version, then the menu won't appear on-screen. It will still be usable, however.

## Style Settings

### Enable Button

For gyro and dpads, this option lets you choose what button activates the on-screen menu
(on touchpads, you simply... touch the pad). It can be most of the physical buttons on your
controller, as well as an 'always on' option, which will keep the touch menu on-screen at
all times.

### Button Count

Touch menus have several predefined button layouts:
- 2 Buttons
- 4 Buttons
- 7 Buttons
- 9 Buttons
- 12 Buttons
- 13 Buttons
- 16 Buttons

Less buttons means each individual button is larger (and therefore easier to hit with a
touchpad/gyro), but obviously limits your overall binding density. Having more set buttons
than specified total count leads to getting later binds cut-off. Empty buttons are greyed
out and not selectable.

### On-Screen Horizonal/Vertical Position

Determines where on the screen the touch menu will appear. The default values put the touch
menu in the bottom right corner of the screen, but not touching the edges of the game screen.

For the horizontal position slider, all the way left has the left side of the menu hugging
the left side of the game screen, and all the way right has the right side of the menu hugging
the right side of the game screen (or as close as the overlay can manage).

For the vertical position slider, all the way left has the top of the menu hugging the top of
the game screen, and all the way right has the bottom of the menu hugging the bottom of the game
screen (or as close as the overlay can manage).

### Menu Activation Style

Controls when the selected binding is activated. Some of the settings utilize an 'activating button'.

- For touchpads, the activating button is the pad click
- For gyro and dpad, the activating button is selectable via the "Menu Activation Button" under
  "Advanced Settings" from the main style settings screen.

#### Button Click

Fires the selected binding when the activating button is pressed, and acts like any normal
button in terms of multi-presses and holds.

#### Button Release

Similar to button click, but the binding is momentarily fired and only when the activating
button is released.

#### Touch Release/Modeshift End

This option briefly fires the selected binding when the touchpad or enable button is released.
Do not use this mode on an always-on gyro/dpad touch menu, as it's not possible to "release"
the always on "button", and the menu will be unusable as a result.

#### Always

Continuously presses the selected binding without needing any additional button presses/releases.
Be mindful of long press/release activators when using this mode.

### Display Binding Label on Button

An on/off toggle that controls whether or not the underlying binding is displayed to the player.
If 'on', then the underlying button will be shown to the player (diminished in the corner if there
is an assigned icon). If 'off', then only the icon will be displayed, or no image at all if the button
does not have an icon associated with it.

### Menu Opacity

Controls how transparent the menu is on screen. All the way left is completely invisible, all the way
right is completely opaque. The default value is ~85% opacity.

### Menu Size

Determines how big the menu is on the screen. Values further to the left make the menu smaller, and
values further to the right make the menu bigger.

### Menu Buttons

The 'menu button' areas are where the binding menus for each of the individual buttons are. These are
full binding menus with the full power of activators. The first 4 buttons are on the first screen with
the rest of the style settings. The rest of the buttons are found in the 'Additional Settings' button.
