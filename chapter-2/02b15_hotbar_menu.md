# Chapter 2b - Section 15: Hotbar Menu

Hotbar Menus are the latest iteration input styles that aim to create a lot of virtual
buttons out of less physical inputs. Where Touch Menus were geared towards the Steam
Controller touchpads, and Radial Menus were geared for analog sticks, Hotbar Menus are
designed to be used with dpads and button diamonds. This input style can also be used on
touchpads, analog sticks.

*[ Sora's note: there are better input options for pads and sticks, and I would recommend
  using touch or radial menus for the other inputs, where you can make good use of their
  analog nature to more fluidly select bindings. Touch and radial buttons both have basically
  equal activation time for all bindings, whereas hotbar menus require you to scroll from
  item to item individually. There's also no option to toggle whether you need to merely
  touch or fully click on a trackpad, so this may be a tiring input to use on a trackpad. ]*
  
The bottom button (or bottom quadrant on a pad/stick) opens the menu. The left and right
buttons (or side quadrants) moves the cursor left and right. The up button (or top quadrant)
activates the button that is currently selected.

This on-screen display requires the Steam Big Picture Mode Overlay to be functioning and
available. If the overlay can't be used with your game, or the overlay is the regular
desktop version, then the menu won't appear on-screen. It will still be usable, however.

## Style Settings

### Hotbar Menu Button Count

A menu that contains several predefined options:

- 2 Buttons
- 4 Buttons
- 7 Buttons
- 9 Buttons
- 12 Buttons
- 13 Buttons
- 16 Buttons

Having more set buttons than specified total count leads to getting later binds cut-off.
Empty buttons between used buttons are greyed out and not selectable, while unused buttons
at the end of the menu are completely unshown.

### On-Screen Horizonal/Vertical Position

Determines where on the screen the hotbar menu will appear. The default values put the hotbar
menu in the bottom right corner of the screen, but not touching the edges of the game screen.

For the horizontal position slider, all the way left has the left side of the menu hugging
the left side of the game screen, and all the way right has the right side of the menu hugging
the right side of the game screen (or as close as the overlay can manage).

For the vertical position slider, all the way left has the top of the menu hugging the top of
the game screen, and all the way right has the bottom of the menu hugging the bottom of the game
screen (or as close as the overlay can manage).

*Note: the defaults for these sliders will tend to have the menu shoot off the side of the screen,
especially if you have a menu with more than ~2-4 buttons on it. It's recommended to adjust the
horizontal slider to the left so that the menu doesn't get cut off.*

### Wrap When Scrolling

A boolean toggle that controls what attempting to 'run off the edge' of the hotbar menu will do.
If this option is 'On', then trying to go past the end of the menu will cause the cursor to jump
to the opposite side, akin to the endless scrolling of a scrollwheel. If this option is 'Off', then
the cursor will not do this. and you must go back the opposite direction.

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

### Dismiss After Activation

Found in the 'Additional Settings' area, this boolean controls whether or not the menu will close itself
when the menu is activated. If 'On', then the menu will close itself after activating the menu item. If
it is set to 'Off', then the menu will remain open until explicitly closed with the bottom button/quadrant.

### Recenter On Menu Dismissal

Also found in the 'Additional Settings' area, this boolean controls the behavior of the cursor when the menu
is re-opened. If it is set to 'On', then the cursor will automatically be placed in the middle of the list, or
a button that is close to the middle. If it is set to 'Off', then the menu will remember where the cursor was
and place it on the button it was last on.
