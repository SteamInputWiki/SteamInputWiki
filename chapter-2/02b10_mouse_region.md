# 02b10 Mouse Region

This Input Style allows the user to map the entire surface of your Touchpad to a segment of your screen. By default your Mouse Cursor will snap back to center when lifting off the Pad as well as when becoming active on your configuration.

Mouse Region is most comparable in function to Touchscreens in terms of base function.

**_!! CAUTION !!_** Although this Input Style can be applied to Button based Input Sources, because they lack analog variables, the Mouse Cursor will only ever move to the maximum of their allowed directions.

Gyro sources also do not seem to function properly. Rather than functioning in a smaller more enclosed square in front of the user it requires the user to physically move the controller much farther than should ever be necessary.

## Region Size

Region Size controls the physical space that your Mouse Region will be mapped to.

Increasing the slider allows the Mouse Region to encompass more of the screen while decreasing forces it to encompass less of the screen.

## Click Binding

Click Bindings work mostly like they would with any other Input Styles, and truly only function properly on touch based Input and Joysticks.

The Click Binding is applied when the touch-based Input and Joysticks is physically depressed. For other non-touch based Inputs because the only way to utilize Mouse Region is to depress the buttons; it will be applied at all times while using Mouse Region.

## Touch Binding

Touch Bindings work just like they would with any other Input Styles, and truly only function properly on touch based Input.

The Binding is applied while physically touching the Input source, or for Input sources that don't have a way to read touch, it is applied when the Input source is used in any manner.

## Horizontal Position

The Horizontal Position slider controls the physical space the mouse region will encompass on the horizontal axis.

Moving the slider to the right will move the Mouse Region to more to the right of the screen while moving the slider to the left moves it to more of the left side of the screen.

## Vertical Position

The Vertical Position slider controls the physical space the mouse region will encompass on the Vertical axis.

Moving the slider to the right will move the Mouse Region to more to the top of the screen while moving the slider to the left moves it to more to the bottom of the screen.

## Region Scale

Region Scale controls the length and width of your mouse region. We can specify how long we want our vertical and horizontal axis to be or even control the shape of how our Mouse Region will be outputted.

Depending on how we adjust our settings it can be much more linear, rounder, or even more square.

### Region Horizontal Scale

The horizontal scale setting controls the horizontal width of the mouse region.

Moving the slider to the right will make our Mouse Region wider than it is taller, while moving the slider to the left will make it taller than it is wider.

### Region Vertical Scale

The Vertical Scale setting controls the vertical length of the Mouse Region.

Moving the slider to the right will make the Mouse Region longer than it is wider, well moving the slider to the left will make it shorter than it is wider.

## Mode Shifting

Mode Shifting allows us to apply a secondary Input Style, either when holding a certain button or using a certain Input type.

Within the secondary Input Style we can make basically any changes to Input we want and it will generally use the settings that apply to that Input Style, optionally we can apply another Mouse Region and change the settings as we desire.

## Haptics Intensity

The Haptics Intensity setting controls the strength of haptics when using Mouse Region.

It's important to note Mouse Region as it is presented by default within Steam Input does not feature any customized haptics, but instead uses the default haptics for standard mouse.

## Outer Ring Binding

The functionality of how Outer Ring Bindings work don't seem to be modified versus how they react when applied to other Input Styles.

The Outer Ring Binding is applied when a certain threshold is met by the user and can be visualized as a virtual circle on the outer edge of your Input method.

### Outer Ring Binding Radius

The outer ring binding radius controls how far out or how soon your Outer Ring Binding circle is versus the center point of the Input method.

Increasing the slider to the right moves the circle farther out, while decreasing the slider to the left moves the circle closer to your Input methods center position.

*[QuizzicalCube’s Notes: By setting the Outer Ring Binding radius to max, while using soft presses as part of our outer ring binding, this allows them to have the full range of the Touchpad when deciding where to activate.*

*A great tip for Mouse Region is to have either a Soft Press or a Normal Press with the desired Ring Binding radius set and an Empty Binding applied.*

*We can apply any Haptic to this Empty Binding and if we move its activation zone to farther range of the Input we can actually feel when our cursor hits the edge of the Mouse Region.]*

### Outer Ring Binding Invert

This setting tells Steam Input whether or not we want to invert how our Outer Ring Binding is applied.

Using this invert option rather than applying our Binding after we hit our virtual circle, it applies while we're not touching this threshold circle and removes the Binding once we hit our applied threshold.

## Snap Mouse To Region On Mode Activation

This setting will determine whether or not the cursor is recentered to the middle of your Mouse Region when it becomes active in your configuration. Please keep in mind this is intended to be used with several higher functioning feature sets of Steam Input such as Layers and Mode Shifting.

A Mouse Region is considered active by Steam Input not necessary when it is receiving input from one, but rather when a Mouse Region becomes present in the configuration. As a result this setting may not come into play during normal gameplay.

## Snap Mouse Back on Stop

This setting will determine whether or not the cursor should be placed back in its original spot it was in prior to the player activating a Mouse Region.

The snap in the name seems to refer to the speed at which the cursor is returned, a process that is handled almost instantly.

## Mouse Dampening

Mouse Dampening allows the user to set a certain Mouse Sensitivity that is only applied when a Trigger is used.

The intended use case is to keep the player in control of Mouse Inputs while firing in game. Many players find the action of clicking the Triggers to slightly move their thumbs and shake the Controller, making Gyro and general Mouse movement less accurate.

### Trigger Press Mouse Dampening

This setting allows the user to choose whether or not mouse dampening is applied and which specific button or trigger will be used to enable it.

### Trigger Press Dampening Amount

The Mouse Dampening Amount tells the steam input how much of a percentage to suppress Mouse Input.

Moving the slider to the right increases the dampening effect while moving it to the left decreases the effect.
