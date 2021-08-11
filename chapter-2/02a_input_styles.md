# Chapter 2a: Input Styles

## Introduction

Certain input devices are capable of being used in a variety of different ways. You could use a physical
joystick as not only a joystick, but also as a simulated D-Pad, a simulated mouse, or more complicated
uses such as a circular scrolling device.

Steam Input calls these different ways of using a physical devices*Input Styles*. Said Input Styles are
pre-defined ways that a physical device can be configured to behave as.

## Which devices can have input styles applied?

The following devices are capable of using input styles:
* D-Pads
* Face button cluster (The lettered ABXY buttons on Xbox and Nintendo controllers, and the X-Circle-Square-Triangle buttons on Sony controllers)
* Analog Sticks
* Trackpads, both the Steam-Controller-style primary use pads and the Sony-style secondary use pads
* Gyroscopes

Not every device supports using every input style.

## What are the input styles available to me?

### Legacy Mode Input Styles

These are what you have to play with for games that do not provide a SIAPI implementation. Each
is more thoroughly documented in it's individual section later on in the chapter.

#### None

Completely disables the input device altogether. If you do not need an input device, this is the
easiest way to disable it so that it does not get in the way of the game, and 'soft documents'
that it is unused in the configuration screen.

#### Directional Pad

Provides an interface that resembles a traditional d-pad. On analog devices like trackpads and sticks, it
has several other options available that provide additional means for packing in movement options.

*Note: the Directional Pad input style does not provide any options to perform Simultaneous Opposite Cardinal
Direction (SOCD) cleaning. This means that unless the input device somehow physically prevents you from doing so
(as a real D-Pad would), it is entirely possible to press both the 'left' and 'right' binds (or 'up' and 'down'
binds) and Steam will send both to the game. This shouldn't be an issue for recent native PC games (which ought
to have native SOCD cleaning built-in), but it could lead to bugs/brokenness in old or emulated games.*

#### Button Pad

Provides an interface that resembles a traditional face button cluster. On touchpads, you can configure
the size and relative distance of the buttons.

#### Joystick Move

Provides an interface that resembles and outputs a traditional joystick. Like the Directional Pad style,
there are additional options that provide greater flexibility and action density.

#### Joystick Camera

Similar to the Joystick Move style, but tweaked so as to be a better experience for controlling a 3rd person
camera, most notably by making the initial contact point the center of the virtual joystick, turning it into
more of a relative style than an absolute style.

#### Mouse

Provides a means of moving your system mouse cursor. This input style contains lots of options, including
accerlation curves and an optional trackball mode.

#### Mouse Joystick

Similar to the above 'Mouse' input style, but instead of sending mouse movement events to the game, it instead
sends a series of joystick 'flicks'. This input style is meant to be used when a game won't accept mixed input,
and its performance and feeling is highly dependent on what the game does to process its joystick inputs. This
style is generally considered a last resort.

#### Scroll Wheel

Emulates a scroll wheel as you'd find on a mouse. This input style can be driven by horizontal, vertical, or circular
motions. You can have either a 'forward/backward' scroll style, or a list of binds that are cycled between.

#### Touch Menu

Using the Steam Overlay, this input style provides a grid menu on-screen to select different actions. This enables
a method to achieve a high action density by allowing up to 16 different buttons on a single input.

This input style does not work on joysticks, where you must use Radial Menus or Hotbars, or on D-Pad/face button
clusters, where you must use Hotbar Menus.

*Note: this input style requires the Steam Big Picture Mode Overlay to function correctly. The regular Steam Overlay,
or no overlay at all, will result in nothing showing up on screen.*

#### Mouse Region

This input style turns a device into a 1:1 positioning tool for the mouse in a pre-defined area of the screen. This
is useful for things like moving the viewpoint on an RTS mini-map.

#### Radial Menu

Similar to Touch Menus, but exposes the individual buttons in a circular pattern usable by joysticks. You may also use
this input style on touchpads; it's merely preference at that point. Provides up to 20 buttons.

This input style does not work on D-Pad/face button clusters; you must use Hotbar Menus instead.

*Note: this input style requires the Steam Big Picture Mode Overlay to function correctly. The regular Steam Overlay,
or no overlay at all, will result in nothing showing up on screen.*

#### Single Button

Turns a trackpad into a single large button.

#### Flick Stick

Created by YouTuber and developer Jibb Smart, this input style turns a joystick or trackpad into an 'absolute turning device'.
Pulling straight back on the stick results in your character turning 180 degrees, pushing it left results in a 90 degree left turn,
and so on. This style is meant to be paired with gyro aim in 3D action games, and is not intended to function standalone.

*[ SoraFirestorm's note: you **can** apply this style to a Steam Controller trackpad (you can to the DualShock 4/DualSense pad
as well, it's just not ergonomically viable there), but the Steam Controller trackpads do not suffer from the inherent bluntness
in trying to use a joystick to aim, so there's not really much point in using this over mouse/mouse-like joystick on SC pads from
my point of view. ]*

#### Directional Swipe

Similar to the Directional Pad style, but requires some travel of an analog input before the actions will be fired. This required travel
makes it more consistent for use on the gyroscope, which is the likely intended usecase for this style.

#### Hotbar Menu

Provides an on-screen scrollable bar menu usable by D-Pad/face button clusters. Can also be used by touchpads and joysticks. Provides up
to 16 buttons.

*Note: this input style requires the Steam Big Picture Mode Overlay to function correctly. The regular Steam Overlay,
or no overlay at all, will result in nothing showing up on screen.*

### SIAPI Mode Input Styles

Games that implement the Steam Input API natively provide their own input styles specific to their game. Most of the
legacy mode input styles will be hidden, but by activating the 'Advanced Settings' via the prompt at the bottom of the
screen, applicable legacy mode styles will reappear, as well as additional settings for the game-provided styles, if
available.

Valve has also added some reimplementations of legacy styles that are available for SIAPI styles (notably providing
'Mouse Joystick' companion styles for joystick-like styles) to work around SIAPI implementations that do not follow
the documented best practices or are otherwise broken.
