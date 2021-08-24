# 02b05: Joystick Mouse

Recommended Watching: (there are no videos specific to this mode, however Joystick Mouse is essentially just Joystick Move with its output hardcoded to Relative Mouse HOWEVER linking videos that cover joystick move might cause confusion…)

This Input Style takes a directional input and converts it to relative Mouse movement. It is intended as a compatibility mode to allow traditional dual stick controllers to play games that only support keyboard and mouse.

This Input Style can only be applied to:

* Joysticks
* Face Button Set
* Directional-Pad

When applied to Joysticks, you can think of this Style as using the Joystick to push the Mouse cursor around the Desktop with full analog control.

The above is also true for Face Button Sets and Directional Pads, however they are restricted to one speed, the maximum possible, and 8 directions.

## Settings

All settings are available to all 3 Devices that can use this Input Style.

### Click Action

It allows you to bind an action to clicking the Joysticks button, or any of the face buttons or d-pad directions.

If using a Joystick for aiming and the game uses the joystick click for an action, a typical use of the click action will be to assign the joystick click to the click action, however as this Input Style is mostly for compatibility the user may assign the equivalent keyboard button instead.

!! CAUTION !! When this Style is being applied to a Face Button Set or D-Pad, any input will activate this Binding as all inputs with those Devices are clicks.

### Outer Ring Binding

For the Joystick, this Binding Activates whenever the user has tilted the Joystick past a defined threshold.

!! CAUTION !! When this Style is being applied to a Face Button Set or D-Pad, any input will activate this Binding as all inputs with those Devices will be considered at the maximum value which will always be beyond the defined threshold.

### Mouse Sensitivity

This slider sets the maximum sensitivity of the relative Mouse movement. Think of it as a dpi setting for a desktop mouse, only as a slider instead of set values

### Mode Shifting

This allows you to set a button to Mode Shift the input device into an entirely different Input Style. Mode Shifting is covered in more detail in chapter 4.

### Haptics Intensity

Haptics in this Style pulse with varying strength depending on how much of the maximum sensitivity you are currently at. So for example with a Joystick barely tilted it provides a very weak “tick” and when the Joystick is fully tilted it provides a very strong “thunk”.

This setting has 4 options that determine how strong that tick/thunk is:

* Off
* Low
* Medium
* High

[Mennenth’s Notes: I… I don’t know what to say. The Haptics Intensity setting only affects the Steam Controller’s haptics, and no Steam Controller user would ever be using this compatibility Style as we already have Inputs that are capable of directly outputting Mouse instead of needing conversion. However, this Style can still be applied to Joysticks so I tested this out on the Steam Controller’s left Joystick… for science! And… It was such a bad feeling. It is basically trying to let you know how far you have tilted the Joystick, but the Joystick itself already gives you that feedback by way of pushing back against your thumb and of course hitting the Joysticks “wall” that prevents it from tilting further. So, no Joystick user would need Haptic feedback anyway.

I have a feeling though, and I think I know why Haptics Intensity was included. As will be discussed in the Joystick Move chapter 02b06, I think this Style is just copy/paste Joystick Move only with its output hard coded to be “relative mouse”. Ignoring the relative mouse part, Haptics Intensity is pretty important when considering the idea of assigning Joystick Move to a Touchpad; the Haptics then help give the user a sense of how far from the center of the Touchpad their thumbs are. So…

For the user of a traditional dual stick controller who is using this Style? I say ignore the Haptics Intensity setting all together/turn it off.]

### Output Axis

This drop down allows you to select which Joystick axis, x and y, cause mouse movement.

It has 3 options:

* Both Horizontal and Vertical - works as normal
* Horizontal Only - only outputs on the x axis
* Vertical Only - only outputs on the y axis

Horizontal Only is how Splatoon 2 works when using Gyro Aiming. The Joystick basically becomes a “fast turn” input and the Gyro handles all the precision/aiming tasks.

### Stick Response Curve

This setting changes the Response Curve of the Joystick. More relaxed curves allow for more precision with small movements, while more aggressive curves result in reaching the maximum output faster when speed is preferred over precision.

It has 6 options:

* Linear
* Aggressive
* Relaxed
* Wide
* Extra Wide
* Custom

!! CAUTION !! Custom then gives you a slider, details below, but that pushes all the options further down in the UI which can make them hard to see or interact with.

### Custom Response Curve

Only visible if “Custom” is selected in the Stick Response Curve setting.

This slider gives you finer control over the Response Curve.

### Dead Zone Shape

This setting allows you to customize the Dead Zone of your Joystick, specifically the shape.

It has 3 options:

* Circle
* Cross
* Square

A Circle Dead Zone results in an even response across the entire throw range of the Joystick.

A Cross Dead Zone emphasizes the cardinal directions more, which is useful for games where you may be holding a cardinal direction for long periods of time.

A Square Dead Zone emphasizes the diagonals a bit more.

[[Mennenht’s Notes: Given the output of the Joystick is a Mouse when using this Style, I would recommend generally setting this to Circle. The other Dead Zone Shapes could be used if the game responds to the Mouse in a way that is not uniform though.]

### Enable Deadzone

This setting is a relatively new addition to Steam Input… and seems to be bugged as the name and description are whack.

In the face of the ever growing “stick drift” issue, Valve has included a way to calibrate the dead zones on your controllers sticks. Details on the Calibration feature can be found in chapter 0e.

The Enable Deadzone setting has 3 functions based on its options.

* None - the Dead Zone is disabled completely; this is for Touchpad users.
* Calibration - if you have calibrated your controllers Dead Zones, that calibration will be used. The configuration defaults to this when you have calibrated your controller.
* Configuration - if you would rather handle the Dead Zone on a per configuration basis, use this setting and the sliders beneath the drop down box for this setting.

If you have not run the calibration, it is highly recommended you do so. Once you have, it is highly recommended to set this option to “Calibration” if it is not already on that option.

### Dead Zone Inner

This slider determines how big the Dead Zone in the center of the Input Device is. All the way to the left is no Dead Zone, all the way to the right and the Input Device is basically disabled.

[Mennenth’s Notes: As the Enable Dead Zone and Calibration features are new and I do not typically play with a Right Joystick, I am unsure how the Dead Zone Inner acts when Calibration is selected. My gut says that Calibration overrides this slider, but I could also see the two being additive; ie, Dead Zone Inner makes the Calibrated Dead Zone larger.]

### Dead Zone Outer

Despite its name, this slider does not create a Dead Zone around the edge of the Input Device but rather defines how far away from the center of the Input Device is considered to be the maximum output.

!! NOTE !!

The effective “throw range” or “analog values” get stretched or compressed to be in between the Inner and Outer Dead Zones. To gain the most precision possible, minimize the Inner while maximizing the Outer. To gain the fastest possible “0-100”, have the Outer be basically on top of or lower than the Inner. Steam Input is smart enough to not break when the Outer is less than the Inner.

### Invert Horizontal Axis

This setting has 2 options:

* Off
* On

When on, the horizontal - or x - axis gets reversed; right becomes left, and left becomes right.

### Invert Vertical Axis

This setting has 2 options:

* Off
* On

When on, the vertical - or y - axis gets reversed; up becomes down, and down becomes up.

!! CAUTION !! Be mindful of any in-game settings that also invert the y axis, as they can cancel each other out.

### Sensitivity Horizontal Scale

This slider determines how sensitive the horizontal - or x axis - is relative to the Mouse Sensitivity slider. All the way to the right, the horizontal axis can reach the maximum sensitivity as set by the Mouse Sensitivity slider. As the slider moves to the left, the horizontal axis’ maximum sensitivity will be decreased until all the way left where it becomes disabled.

### Sensitivity Vertical Scale

This slider determines how sensitive the vertical - or y axis - is relative to the Mouse Sensitivity slider. All the way to the right, the vertical axis can reach the maximum sensitivity as set by the Mouse Sensitivity slider. As the slider moves to the left, the vertical axis’ maximum sensitivity will be decreased until all the way left where it becomes disabled.

### Outer Ring Binding Radius

This slider sets where the threshold is along the output value. To the right it is nearer to the edge of the Input Device, and to the left it is nearer to the center.

### Outer Ring Binding Invert

This setting has two options:

* Off
* On

When on, the Outer Ring gets inverted and becomes a sort of “center binding”, where the binding is activated whenever the Input Device’s output is on the center side of the radius instead of the edge side.

!! NOTE !!

When this Style is used on a Face Button Set or Directional Pad, the Outer Ring Binding seemingly becomes disabled.

### Output Anti-Deadzone

Sometimes, a game will apply a Dead Zone to camera movement. This slider effectively adds extra movement to your Input in order to counter that Dead Zone. Think of it like a “minimum output value”. You should consider raising this slider if the input feels “mushy” when trying to make small precise movements.

### Output Anti-Deadzone Buffer

If you have applied Anti-Deadzone, you can use the Buffer to re-establish a Dead Zone. To mis-quote Adam Savage of Mythbusters fame “I reject your deadzone and substitute my own!”

[Mennenth’s Notes: Before messing with the Dead Zone Inner slider, double check to see if the game is applying its own Dead Zone. If it is, then the Anti-Deadzone settings should be preferred while Dead Zone Inner should probably be left alone.]

## Overall Mennenth’s Notes

This Input Style is a bit of a weird one truth be told.

As mentioned, it is really supposed to be a compatibility Style for Joystick users trying to play games that only accept keyboard and mouse inputs. When used, it allows the Joystick to feel like a Joystick while the game sees a mouse. It is kind of the opposite of the previous Style, Mouse-Joystick (chapter 02b04).

However, what is weird about it is that a lot of the settings are more geared towards how a Joystick functions and not really how a Mouse functions. As I mentioned in my note about Haptics, it seems this Style is a copy/paste of the Joystick Move Style, only with its output hard coded to Relative Mouse… which means that hypothetically this Style does not really need to exist… outside of maybe staving off confusion due to naming conventions? I don’t know.

Regardless, if you are using a controller that is more the traditional dual stick type and you are playing a game that only accepts keyboard and mouse inputs… this Style will get you playing pretty immediately.
