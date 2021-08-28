# 02b11 Radial Menu

This Input Style allows the user to create a Radial Menu of varying sizes and transparency. Radial Menus are circular menus that hold various actions and allow for quick selection of said actions. 

Radial Menus work in much the same way as Weapon Wheels, which are often seen within modern game design and can be used for any types of actions the player desires. These can be comprised of any Bindings available to other forms of Input, including different types of Activators. 

Some actions that work well when bound to Radial Menus are weapon selection, Ingame Abilities, and Hotkeys. Each action can be given an icon that will be displayed on the action when rendering the Radial Menu. Names on each action will be shown during render as well. 

They can be applied to
* Touchpads
* Joysticks
* Traditional D-Pads
* Traditional Button Pads

When applied to Touchpads and Joysticks they work in the way you’d expect, with tweaks on functionality depending on the applied settings. The player selects an action that has been bound in their Radial Menu by sending Input in the direction of said action.

With Traditional D-Pads and Traditional Button Pads, Radial Menus will work quite a bit differently while applied to these Input Sources. Setting changes such as Menu Activation Style can be applied, however do not always work as expected. It is mostly only useful for giving your Button presses an On-Screen Display.

## Menu Buttons (up to 20)

Our Menu Buttons are the actions we wish to have on the Radial Menu. How they can be selected may change based on the Menu Activation Style we set, however we can choose different types of Activators to change the order of Grouped Bindings on Activation.

On Button based Input Sources only up to eight Menu Buttons should be used. Although more can be applied, in order to select non cardinal direction Menu Buttons two Input Buttons must be used, therefore it is not functional possible to use more than eight.

Much like normal Bindings, here we are allowed to give them a name along with a feature exclusive to Menu Inputs Styles and Steam Link Virtual Buttons, Menu Icons. Each Menu Icon is rendered to represent the Binding on the Radial Menu and can be given custom colors by the user.

*[ QuizzicalCube’s Notes: By setting custom Menu Icons in a folder named “touchmenuicons”  in the first folder of your games directory, these icons will only  appear for this game and will placed on top of available icons for this game. ]*

### Nesting Touch or Radial Menus

By adding either an Action Layer or an additional Action Set we can nest one Radial Menu inside another. We do this by adding a Binding to apply this layer on our Radial Menu, then adding a Binding to remove this layer on the other Radial Menu.

##### Recommend Viewing:
[Radial Menus: Nesting and Cycling - By Critical Input](https://youtu.be/UeTUQX45Cwk "Radial Menus: Nesting and Cycling - By Critical Input")

[Two Pad Menu System: An Adaptation of Nested Menus - By Critical Input]( https://youtu.be/7vxEGvnfwH8 "Two Pad Menu System: An Adaptation of Nested Menus - By Critical Input")

## Menu Activation Styles

Menu Activation Styles allow us to tell Steam Input how we’d like to select the Bindings from our Radial Menu. The following will be brief descriptions of how each style reacts.

### Button Click

The Button Click setting will force the user to click in on the direction of the desired Input action on the Radial Menu in order to select an action. This setting doesn't have any functional effects on Button based Input Sources as we must click in our Buttons to select regardless.

### Button Release

The Button Release setting will tell Steam Input to use the Binding we are touching once we release our desired Input method. This setting works very well with Touchpads and Joysticks, with Button based Inputs however non-cardinal directions do not seem to fire very accurately and may make selecting them very difficult.

### Touch Release/Modeshift End

With this Activation Style, our Binding is only selected when either the player lets go of the Radial Menus current Input Source or a Modeshift occurs.

### Always

The Always Activation Style will allow the user to select Bindings simply by touching, pushing, or clicking the Input of their choice in the direction of that Binding. 

*[ QuizzicalCube’s Notes: Each Binding will always fire as soon as it is selected so it is advisable that the player either be deliberate with how they use this Menu Activation Style or use it with Bindings that can easily be spammed with no consequences. ]*

## Visual Settings for Radial Menus

### On-Screen Horizontal Position

When using the Horizontal Position slider, a decrease will move our Radial Menu on screen further to the left, while an increase to the slider will move it to the right.

### On-Screen Vertical Position

When decreasing the Vertical Position, our Radial Menu will render higher up on the screen, while increasing the slider will move the Menu farther down.

### Menu Opacity

The Menu Opacity slider controls the level of transparency when rendering the Radial Menu. Sliding to the left will make the menu more transparent, while sliding to the right will make it less transparent.

### Menu Size

The Menu Size slider controls the size our Radial Menu will render at. Sliding to the left will make the menu smaller, while sliding to the right will make the menu larger.

### Display Binding Label on Button

This setting controls whether or not the Bindings actual name is displayed while rendering the Radial Menu. These labels will appear on top of the Menu Icon of each Binding and Inputs with larger names may appear to have visual issues. 

The name on these labels will always be the name of the Input used with this setting and should not be confused with the Binding name, which is the name given by the user.

## Additional Buttons

### Center/Unselected Button

This Binding will determine what or whether an action will be sent when no direction is selected in a Radial Menu, or when the center is selected. Much like Menu Buttons a Menu Icon and name may be given. 

### Click Action

The Click Action is intended for when touch-based Input is used to select Menu Bindings. The Click Action is a Binding that will register anytime the Touchpad or Joystick is clicked. For button-based Inputs the Click Action will register at any point the Input is used.

## Dev Implementations

Even for games with Native Steam Input, Developers can make use of Radial Menus within their shipped configs. This may not look as good as what you can do Ingame with built-in Radial Menus, however it is quicker to implement and you can also ship custom Menu Icons within your builds.
