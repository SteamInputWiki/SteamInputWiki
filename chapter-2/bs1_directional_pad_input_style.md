# 02b01: Directional Pad

Recommended watching:
<links to my dpad settings videos, critical inputs, woodsies...>

This input style functions how a dpad would; 4 directional buttons with
overlapping diagonals that hold the cardinals as you move from cardinal to and
adjacent diagonal to the adjacent cardinal.  It gives you 4 binding slots in the
cardinal directions that activate and mix according to the above.

It can be assigned to:
* traditional dpads
* traditional abxy button pads
* joysticks
* touch pads
* gyro

When applied to traditional dpads, it functions exactly how you would expect.

When applied to button pads, it does send everything so how simultaneous
opposing cardinal directions (socd) works depends on how the game you are
playing handles it.

When applied to an input device with xy coordinates, the output values are
divided into "zones". The shape of those zones will be explained shortly. socd
cannot happen on these due to only being able to send 1 set of coordinate values
at a time.

When applied to the gyro, the controller itself becomes the dpad. Think of the
top of the controller that your thumbs interact with as being the top surface of
a dpad and the back of the controller being where the buttons are. From there
you tilt the controller in the direction of where the button would be.

## Shared Settings

Unless otherwise noted, these settings are available to all input devices

### Bindings

The default bindings are the xinput dpad directions. These can be changed to
wasd on the keyboard, or any other binding, if you'd like by navigating to the
direction and selecting it. For a more detailed break down of bindings, please
see chapter 03.

### Layout:

This setting is available to all input devices, however not every layout is available to every input device; exceptions will be noted.

#### 8 Way (Overlap)

This layout divides the xy coordinates like a pizza or a pie would typically be
divided, into 8 wedge shaped slices. A slice is at each cardinal for 4, and then
each diagonal for 4 more.

#### 4 Way (No Overlap)

This layout is similar to 8 way, only it lacks the diagonals. 

#### Cross Gate

When applied to devices with xy coordinates, it divides them in a tic tac toe
board shape, or a square 3 by 3 grid.

When applied to traditional dpads or button pads, it has some extra code for
handling hysteresis/debouncing of the buttons for more reliable dpad function.

#### Analog Emulation

Not available to traditional dpads and button pads.

This layout doesnt really divide the xy coordinates into specific zones but
rather blends them together by rapidly activating and deactiving, referred to as
"pulsing" from here on, the bindings to emulate a more analog like response; the
pulses are slower paced towards the center and faster paced towards the edge,
and the bindings are proportionally pulsed depending on the "angle" in order to
expand the dpad from 8 directions to as full 360 degrees as it can.

Basically, its trying to replicate how an analog stick would work.
	
### Overlap Region

Not available to traditional dpads and button pads

Despite wether or not the slider is visible, this slider only impacts the 8 way
(overlap) layout. It determines how big the cardinal wedge slices are relative
to the diagonal wedge slices. At its default value, cardinals and diagonals are
equally sized. Lowering it makes the cardinals bigger until its almost the same
as 4 way by having really huge cardinal zones, increasing it is obviously the
opposite; it makes it so the diagonals become really huge.
	
### Modeshifting

this allows you to set a button to modeshift the input device into an enitrely
different input style. Modeshfting is covered in more detail in chapter 4.
	
### Haptics Intensity

Only works with the Steam Controller's haptics

The haptic actuators in the controller pulse whenever the input gets activated
or de-activated. This setting determines the strength of that pulse. Off, low,
medium, and high are all pretty self explanatory. The default of "Use Activator
Settings" means the activators own haptics setting overrides this setting, and
activator haptics are defaulted to off. Activators will be covered in more
detail in chapter 4.
	
### Click Action

Not available to Gyro

This is a binding for whenever the input devices button(s) is clicked.

For touch pads and joysticks, this binding is activated when you click the pad
or stick. This could be useful for assigning whatever key is the sprint binding
to the click when you are using dpad mode for wasd in kbm only games.

Beware: When assigned to a traditional dpad or button pad this binding will
activate whenever you click any of the buttons. This can be fine if you want a
binding to activate whenever you activate any direction and dont want to go
through the hassle of setting up "multi-button" for each direction, but for
something like the afforementioned sprint binding it means you will never not be
sprinting which may not be desireable.

### Deadzone

Only available to Touch Pads and Joysticks

For touch pads and joysticks, there is a dead zone in the center where no input
will be sent. This slider determines the size of that deadzone.

For 8 way, 4 way, and analog emulation layouts the deadzone is a circle.

Cross Gate layout is special though. While the deadzone slider does change the
size of the deadzone in Cross Gate layout, it also doubles as the "overlap
region" slider. The larger the deadzone, the smaller the diagonals will be. The
smaller the deadzone, the larger the diagonals will be.

### Analog Emulation Pulse Time

Despite visibility, only impacts Analog Emulation layout

This slider determines the pacing of the pulses in miliseconds. For the
musically inclined, you can think of it kind of like a metronome. It will pulse
every x miliseconds, determined by this slider.

### Analog Emulation Active %

Despite visibility, only impacts Analog Emulation layout

This slider determines how long the input is held down during each pulse, as a
percentage of the time in between pulses

*[ To better understand how the two analog emulation sliders interact with each other...*

*Think of it this way: If the Pulse Time is set so its pulsed every 10
miliseconds and the Active % is set to 30%, this means that when the input is
activated, the pulse will look like this: On for 3 miliseconds, off for 7
miliseconds, repeat until the input is deactivated. If Time is set to 6
miliseconds and % is set to 66%, it will be on for 4 miliseconds, off for 2,
repeat. ]*
	
### Outer Ring Binding

Not available to Gyro... bugged?

For traditional dpads and button pads, this functions like the click action.

For input devices with xy coordinates, this binding only activates once you have
crossed a threshold, defined by the radius, towards the maximum output.

### Outer Ring Binding Invert

Not available to gyro... bugged?

This setting is a binary Off or On, with default to off.

If set to on, the outer ring binding acts more like a "center" binding. It will
activate if the position of the xy input is within the threshold, and deactivate
once the xy position is outside the threshold.

### Outer Ring Binding Radius

Not available for gyro... bugged?

This slider sets where the threshold is along the output value. To the right its
nearer the edge of the input, to the left its closer to the center.

*[ When set all the way to the right and then with inversion
 set to on, it covers the entire output value range of the input device. This
 can be useful for the touch pad in particular, as with requires click set to
 off it becomes a general touch binding that can be used in conjunction with the
 click action for 2 extra bindings a traditional physical dpad would not have
 controlled access to. ]*
	
## Gyro Only Settings

### Gyro Enable Button

This setting determines which button on the controller enables the gyro, or it can be set to always on.

### Gyro Button Behaviour

Turns Gyro:
* On: The gyro will only be active when the enable button is held.
* Off: The gyro will be active UNLESS the enable button is held.
* Toggle: The enable button will toggle between gyro on and gyro off.

### Gyro Pitch Neutral Angle

pitch is the Y axis. This slider determines where along the y axis the
controller is considered at its resting state. For example, this allows you to
determine if you want neutral to be when you are laying the controller flat on
your lap or if you are holding it upright like a steering wheel.
