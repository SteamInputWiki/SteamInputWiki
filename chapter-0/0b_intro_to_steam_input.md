# chapter 0b: intro to steam input

## What is Steam Input?

Steam Input started its life as an api and configuration utility specifically
for the Steam Controller and was named accordingly. However, once Valve started
opening up the configurator to other controllers they renamed it to avoid
confusion. These days Steam Input supports not just the steam controller but
also xbox controllers, sony's dual shock 4, sony's dual shock 3 though it
requires the driver from the psnow service, sony's new dual sense controller,
switch pro controllers, and many 3rd party variations of each. It also supports
generic controllers that use dinput, though the user will typically have to map
their inputs to the cooresponding xbox controller inputs before they can
actually get to rebinding them.

It is a software utility that is part of the Steam platform, and when a
supported controller is connected and support for it has been opted into then it
is a controller rebinding suite that has loads of functionality. With it, you
can command your entire pc with just a controller and some configuration work.

It has two components to it, the first being keyboard mouse and gamepad
emulation, and the second being an input api developers can implement in their
games for tighter controller support.

Lets start with the first component.

## At its most basic, what does Steam Input mean to a user?

As a user/gamer, Steam Input at its most basic solves many controller
compatibility issues on pc. I remember having to use motioninjoy and eventually
scptoolkit to use my ds3 back then. Those programs worked, but in some cases
they were finnicky. There are other alternatives out there today as well, and
while they are way better today they still have their own strengths and
weaknesses.

As far as simplicity though, Steam Input handles controller support such that no
other program is needed. If you game on pc you likely have steam, and if you
have steam then your controllers will work once you have opted into support. It
cant really get simpler than that.

It does go beyond simple support though. As has been mentioned, the Steam Input
Configurator allows you to rebind and make profiles for your controllers so you
can really tailor your gaming experience. These profiles include a desktop
configuration for general pc use, a big picture configuration for navigating
steams big picture mode, then profiles on a per game basis, and lastly a "guide
chord" config that is a universal config the controller swaps to when holding
the guide or home button. Full break downs on each type of config will be in
chapter 01.

By taking advantage of all the profiles, Steam Input does allow you to use your
controller in every aspect of your pc.

It does have two potential downsides though.

The first is that it requires Steam to be running, and your games have to be
launched through Steam. This doesnt mean you can't buy your games elsewhere, but
you will typically have to add them to Steam and launch them from there. For me
this isnt much of an issue, but I know for plenty of people it may be.

The second is that there are a some games that dont work with Steam Input at
all. To understand why without getting very technical, in order for Steam Input
to work the Steam Overlay needs to be able to hook into the game, and the game
needs to accept software input.

There are some games that dont allow the overlay to hook and therefore doesnt
work with steam. There are ways around this which will be discussed in chapter
09.

But more annoyingly, there are some games that dont allow software input. The
biggest example is Valorant, which doesnt accept software input. In this case
there is really nothing that can be done, Steam Input simply will not work for
that game.

## At its most basic, what does Steam Input mean to a developer?

For the most part, business as usual.

Since Steam Input handles controller support, if you are launching on Steam then
you dont have to worry about natively supporting a variety of controllers... at
least not as much as you might otherwise. Its still a good idea to have native
controller support when possible though, in case the user hasnt opted into steam
input support. But if they have opted into support, it would be a good idea to
keep them in mind. A couple of things you can do to facilitate their use of
Steam Input was kind of hinted at a couple of paragraphs ago.  Allow the Steam
Overlay to hook, allow your game to accept software input.

There are a couple of other good ideas too that will be discussed more indepth
in a later chapter, but for a couple of other bullet points:

* allow the user to decide on a glyph set for button prompts, or pull the glyph sets from steam (possible to do without implementing the api)
* allow mixed input (ie xinput and mouse at the same time)

by doing all of those things with your steam release, you facilitate people who
want to use steam input to play games.