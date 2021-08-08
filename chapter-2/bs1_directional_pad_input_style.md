# chapter 02b01: Directional Pad

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

The settings for this mode are as follows:

### Bindings

The default bindings are the xinput dpad directions. These can be changed to
wasd on the keyboard, or any other binding, if you'd like by navigating to the
direction and selecting it. For a more detailed break down of bindings, please
see chapter 03.

### Requires Click

This setting is only available for touch pads in dpad mode.

This is a binary Off or On setting, that determines if you need to click the
touch pad in order to send the directional input.

*[ Mennenth's Notes:

The benefits to having it On is that you can touch anywhere on the pad without
sending input. Touching becomes like selecting and clicking becomes like
confirming. This can be helpful in certain situations, however...  because the
touch pad uses your thumbs location in order to determine which input to send
anyway, requiring the click is an extra step that slows down the rate at which
you can make inputs. On top of this, because the touch pads have only a single
physical button beneath their center requiring the click can make transitioning
from one direction to another without stopping input first can feel incredibly
weird as the button is already pressed at that point; you'll get no additional
feedback from the button, and transitioning can be a bit more difficult due to
the added friction from the force of your thumb pressing into the pad. All
things considered, I would recommend turning it off. It will feel weird at
first, but once you get the hang of it your skill ceiling will be higher. ]*

### Layout:

This setting is available to all input devices, however not every layout is available to every input device; exceptions will be noted.

#### 8 Way (Overlap)

available to all input devices

This layout divides the xy coordinates like a pizza or a pie would typically be
divided, into 8 wedge shaped slices. A slice is at each cardinal for 4, and then
each diagonal for 4 more.

*[ Mennenth's Notes: This layout works best when the dpad has been rebound to
 WASD for kbm only games, or for niche situations such as moving abxy to the
 Steam Controllers right touch pad. ]*

#### 4 Way (No Overlap)

available to all input devices

This layout is similar to 8 way, only it lacks the diagonals. 

*[ Mennenth's Notes: This layout works best when the game only uses the dpad for
 things like menu navigation or 4 way quick weapon swap like in the Borderlands
 games or load out swapping like in the Dark Souls games. Also for 2d games that
 only have 4 way movement, such as Baba is You. By removing the diagonals, it
 helps prevent accidental inputs. ]*

#### Cross Gate

available to all input devices

When applied to devices with xy coordinates, it divides them in a tic tac toe
board shape, or a square 3 by 3 grid.

When applied to traditional dpads or button pads, it has some extra code for
handling hysteresis/debouncing of the buttons for more reliable dpad function.

*[ Mennenth's Notes: This is the premier layout for when the dpad is a primary
 control for the game; movement in 2d platformers and fighting games come to
 mind. Because of the grid shaped divisions for the zones, it has consistent
 spacing between opposing directions; ie no matter where your thumb is on the up
 and down axis, the distance between left and right remains the same. If in 8
 way mode, the distance between left and right actually changes depending on
 where your thumb is on the up and down. Consistent distances facilitates
 developing the muscle memory needed to use an xy coordinate input device as a
 dpad. ]*

#### Analog Emulation

Not available to traditional dpads and button pads.

This layout doesnt really divide the xy coordinates into specific zones but
rather blends them together by rapidly activating and deactiving, referred to as
"pulsing" from here on, the bindings to emulate a more analog like response; the
pulses are slower paced towards the center and faster paced towards the edge,
and the bindings are proportionally pulsed depending on the "angle" in order to
expand the dpad from 8 directions to as full 360 degrees as it can.

Basically, its trying to replicate how an analog stick would work.

*[ Mennenth's Notes: I have barely used this "layout", because how well it works
 is highly dependent on the game. It can absolutely work, but it usually results
 in stuttery animation cycles when used for movement. Critical Inputs video in
 the recommended watching does highlight an interesting use case when it comes
 to shmups; in certain shmups it could lead to a higher fire rate than even
 setting a binding to turbo mode could achieve. However, for me personally I've
 always found the other layouts to be much more predictable/reliable/consistent
 overall. ]*
	
#### Overlap Region

Not available to traditional dpads and button pads

Despite wether or not the slider is visible, this slider only impacts the 8 way
(overlap) layout. It determines how big the cardinal wedge slices are relative
to the diagonal wedge slices. At its default value, cardinals and diagonals are
equally sized. Lowering it makes the cardinals bigger until its almost the same
as 4 way by having really huge cardinal zones, increasing it is obviously the
opposite; it makes it so the diagonals become really huge.
	
### Modeshifting

Available to all input devices

this allows you to set a button to modeshift the input device into an enitrely
different input style. Modeshfting is covered in more detail in chapter 4.
	
### Haptics Intensity

Available for all input devices, but only works with the Steam Controller's haptics

The haptic actuators in the controller pulse whenever the input gets activated
or de-activated. This setting determines the strength of that pulse. Off, low,
medium, and high are all pretty self explanatory. The default of "Use Activator
Settings" means the activators own haptics setting overrides this setting, and
activator haptics are defaulted to off. Activators will be covered in more
detail in chapter 4.

*[ Mennenth's Notes: When dpad is being assigned especially to the steam
 controllers touch pads, putting this to anything other than off is HIGHLY
 recommended due to my previous recommendation to turn requires click to
 off. The haptic pulses take the place of the physical feedback an actual button
 would provide, which means they are crucial to getting the "touch dpad" to feel
 as good as possible. You can use the default "Use Activator Settings" mode, but
 you would want to adjust the haptics per activator from there. This can open up
 some interesting options for customizing the feedback you get, though if you
 want to keep things simple then I'd personally use the setting on the main dpad
 page. ]*
	
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

*[ Mennenth's Notes: While a large deadzone could help you avoid unintented
 inputs, it will also make it harder to make rapid inputs. Personal preference
 will play a role in that balancing act, so experiment to see what you find
 best. If you are just starting out you may prefer larger deadzones. As I got
 used to it, I started preferring smaller deadzones to make more rapid inputs. ]*
	
## Additional Settings

### Analog Emulation Pulse Time

Despite visibility, only impacts Analog Emulation layout

This slider determines the pacing of the pulses in miliseconds. For the
musically inclined, you can think of it kind of like a metronome. It will pulse
every x miliseconds, determined by this slider.

### Analog Emulation Active %

Despite visibility, only impacts Analog Emulation layout

This slider determines how long the input is held down during each pulse, as a
percentage of the time in between pulses

*[ Mennenth's Notes: To better understand how the two analog emulation sliders interact with each other...

Think of it this way: If the Pulse Time is set so its pulsed every 10
miliseconds and the Active % is set to 30%, this means that when the input is
activated, the pulse will look like this: On for 3 miliseconds, off for 7
miliseconds, repeat until the input is deactivated. If Time is set to 6
miliseconds and % is set to 66%, it will be on for 4 miliseconds, off for 2,
repeat.

Despite conceptually understanding it, I have never been able to tune analog
emulation well enough for me to personally want to use. If you can, great! But
as I mentioned earlier, for me I find the other layouts more
predictable/reliable/consistent. ]*
	
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

*[ Mennenth's Notes: When set all the way to the right and then with inversion
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
	
*[ Overall Mennenth's Notes:

Directional Pad is a "corner stone" input style that will be used frequently for
a wide variety of games, and dpads in general are pretty make or break for many
people when judging a controllers merits for specific genres such as 2d
platformers.

While the settings found in this mode arent particularly impactful for
traditional physical dpads, they make a world of difference when it comes to
using the steam controllers touch pad as a dpad. Lacking a tradition dpad has
been a pain point for many people trying to use the steam controller, and the
general opinion is that the steam controller is worthless for games that use
dpads as their primary input.

But as demonstrated in the videos linked in the recommended watching section,
the "touch dpad" can perform surprisingly well in those games... with good
settings and once you have adapted to the touch nature of it.

My personal settings for the "touch dpad" when using it for traditional dpad
tasks are pretty simple:

* **requires click**: off
* **layout**: cross gate
* **haptics intensity**: high
* **deadzone**: 3 ticks bellow default

With that and loads of practice, I can speed run difficult 2d platforming
sections and post some pretty respectable times. Its clear that the touch dpad
is not whats holding me back. Moral of the story? If you are willing to take the
time to learn how to use it, the touch dpad is just as good as any other dpad
out there.

If you are setting up dpad mode on a joystick or an actual physical dpad, my
recommendation for settings would be to leave them on the default.

If applied to gyro... it sounds like a fun idea at first but unfortunately you
have to tilt the controller very far to get it to activate. It works, but this
is one of the instances that I would call a motion gimmick. ]*