# Chapter 2b - Section 8: Scroll Wheel

The scroll wheel input style emulates... a scroll wheel, as you commonly find on a lot of computer mice.
It can be used on trackpads and analog sticks.

## Style Settings

### Sensitivity

The sensitivity controls how many distinct click spots there are on the scroll wheel.
Lower sensitivites give you less click spots further apart. Higher sensitivies give you
more click spots close together.

NOTE: In the default desktop configuration for the Steam Controller, the left pad is set
to be a circular scroll-wheel. *However*, whoever made that config decided to bump up the
sensitivity from the style's default 0.5 to 0.888. So if you have utilized a scroll-wheel
style in your config and have been confused by it not 'feeling right' relative to the desktop
config, that's your likely culprit. Just adjust the sensitivity upward.

### Scroll Forward and Scroll Backward Binding

These activators control what is sent to the game whenever the scroll wheel is moved 'forward'
and 'backward'.

### Swipe Direction and Invert Direction

Both of these options are closely related so they will be discussed together.

Swipe Direction determines what kind of motion activates the scroll wheel:
- Circular requires you to move the input... in a circle. By default, clockwise is considered
  'forward', and counter-clockwise is considered 'backward'
- Horizontal requires pure left-and-right movement. By default, right is considered 'forward',
  and left is considered 'backward'.
- Vertical requires pure up-and-down movement. By default, down is considered 'forward', and
  up is considered 'backward'.
  
Analog sticks do not consider motions that return to center as those that activate the scroll
wheel (as one would anticipate).

Invert direction reverses the sense of the direction. This causes the motion that would fire the
'forward' binding to instead fire the 'backward' binding, and vice-versa.

### Spin Friction

Analogous to the 'trackball mode' of the Mouse Input Style, spin friction determines how long the
virtual scroll-wheel will continue to scroll based on the speed the input is released at. The options
are:

- Off (stop spinning immediately on release)
- High
- Medium
- Low
- None (don't stop spinning on release)

Touching the pad/moving the stick from neutral will cause the virtual scroll-wheel to stop immediately,
again, similarly to how 'trackball mode' works for the Mouse Input Style.

### Haptics Intensity

Controls how much feedback you get from a controller's haptics system. The available options are
'Off', 'Low', 'Medium', and 'High'.

### Scroll Sheel Click Action

A binding for when the trackpad or analog stick is physically pressed in.

### Scroll Wheel List Mode

The Scroll Wheel style has a second operating mode. Instead of having just one binding that always
fires when moving forward, and another that always fires when moving forward, it's possible to provide
a list of binds to cycle between. The list binds and extra option are found under the "Additional
Settings" button.

List mode binds will take precedence over the forward/backward binds. If you have both assigned, only
the list mode binds will be sent to the game.

There are 10 slots available to fill with binds for list mode. When the scroll wheel is moved 'forward',
the next highest numbered list slot will be fired. When the scroll wheel is moved 'backward', the next
lowest numbered list slot will be fired.

There is also the Wrap List option. If it is set to 'on', then hitting the end of the list will cause the
next scroll click to wrap around to the other end of the list (going forward, List Item 1 will come after
List Item 10) allowing for an infinite scroll. If it's set to 'off', then the scroll wheel will stop at
the end (nothing will come 'before' List Item 1 or 'after' List Item 10), requiring you to reverse direction
to get to the other list items. There are no haptic events if you continue to move in the direction the
scroll-wheel is stopped.
