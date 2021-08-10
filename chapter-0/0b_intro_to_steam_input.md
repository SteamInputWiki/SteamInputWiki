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

First off, to any developers that may be reading this;

If the Deck is going to be as popular as the hype as making it out to be, then it would behoove you to make sure the Steam Overlay can hook into your game and talk to it over SendInput. See the note about Valorant in the last paragraph? Because the Deck will be using Steam Input for its controls, if Valorant doesnt change its anti cheat to allow software inputs, then Deck users will NOT be able to play Valorant.. At least not on the go when they will not have access to plugging in external gear. If you have any notion that your audience will want to play your game on the Deck, then dont be like Valorant. Moving on.

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

But! There is another layer to Steam Input.

## The API:

Valve also made an entire input API to go along with Steam Input’s configurator. An API is a set of code/tools developers can implement into their games to accomplish a variety of goals. Steam Input is an Input API for handling player input to the game. Another example of an input api is xinput, the highly standardized xbox controller input system that is pretty ubiquitous even in pc gaming.

To understand the Steam Input API, or SIAPI for short, lets quickly talk about xinput.

Xinput basically just defines a set of buttons and analog controls. Abxy, the dpad, 2 joysticks, 2 bumpers, two triggers, start/select/home. When a developer implements xinput into their game, their game can then understand what all those inputs are… but its up to the developer to decide how they get used. For instance, the developer has to take the A button and tell the game what to do when they receive that input. Commonly, “jump” in action games.

SIAPI functions a little bit differently. It can kind of be viewed as the reverse of xinput. Instead of defining a small number of buttons and some analog inputs, SIAPI allows the developer to define a list of actions or input styles that can be used. For instance, instead of saying that the A button is jump, in SIAPI “Jump” is now an action that gets bound to… well whatever on/off button type input the developer/user wants. 

That might not sound like a big deal, but it has a lot of ramifications that in my opinion make SIAPI superior to xinput.

What are the benefits of SIAPI?

## For the User

Previously (and this is still the case with non-siapi), if a user was taking advantage of rebinding tools to customize their controller, then they would have 2 options. A; be limited by whatever rebinding tool is in the game which is typically very basic, or B; use an external to the game utility that is much more feature rich, but then have to deal with “where did I rebind X again?”, or worse have to figure out a rebinding system that works well not just while in the game but also in the games menus.

In a game that has siapi implemented, those issues are completely solved. Steam Input is a much more robust of a rebinding utility than most in-game solutions, and with SIAPI whenever an action gets bound to a different button the in-game prompts can automatically adjust to match. That is the real benefit of binding the “Jump” action over binding the “A” button; the button prompts will also line up with whatever customizations you as a player have done.

A good SIAPI implementation will also have automatic context based Action Set swapping. More on action sets in chapter 4, but remember the previously mentioned dilemma of rebinding where the user would need to balance in game and in menu controls? Action Sets solve that problem entirely, and instead of having to manually swap action sets the developer who implements SIAPI can implement a different action set for each context the game has (in menu, on foot, in vehicle, etc) and have the configuration swap to the appropriate set automatically.
So… The user gains a theoretically seamless controller experience, no matter what controller they are using and more importantly; how they’ve customized or rebound their controls to better suit them. Are there any catches?

Well, unfortunately there are 2.

For the first, as with basic Steam Input itself SIAPI does require Steam to use. This isnt quite the same as with using the basic remapping side of steam input. There you can still buy your games from other stores and add to steam to take advantage of steam inputs remapping. Here, siapi can be found only on steam versions of the game.

The second one though… Unfortunately, as a relatively new API not all developers actually implement it well. When not implemented well, SIAPI can actually be a burden on the player by preventing them from customizing their experience to fit their needs. While there will be a chapter going more in depth on games that have implemented SIAPI, I want to highlight 2 games that are opposites of each other.

Horizon Zero Dawn’s implementation leaves a lot to be desired. It has no actual mouse input style for touch pad or gyro users and doesnt work with mixed inputs. It also hard codes the steam controllers left touch pad as a dpad, preventing the player from customizing it to their needs.

No Man’s Sky… as yet another feather in the cap of their redemption story, Hello Games absolutely knocked it out of the park with their SIAPI implementation. It's still not 100% perfect, but in my opinion it's the gold standard of what siapi implementations should be. It has action sets for every context with an extensive list of bindable actions, and it all works pretty flawlessly. It's actually one of my favorite games to play because the controls are so well done.

## Benefits for developers

As mentioned, implementing siapi ensures support with a wide variety of controllers.

It can also help ensure a very good experience for the people who play your games with controllers (if implemented well).

Now for the downsides for developers;

It was established earlier that siapi is pretty new as an input api. As a result, it can be a bit tricky or otherwise weird to implement. Valve has released documentation to help, which will be discussed in a further chapter. This could eat up dev time more than simply slapping the universal xinput into your game and calling it a day, especially because of the next reason.

Siapi is locked to steamworks, meaning you MUST release your game on steam to take advantage of siapi. This is different from the basic remapping side of steam input. While you dont need to implement siapi to release on steam, if you use siapi only steam customers will be able to use it. Release elsewhere? Well, then you'll need to implement other api's, such as xinput, or otherwise do the work to natively support the controllers you think your players will be using. Therefore implementing SIAPI is spending dev time for a feature not everyone will be able to use.

If you are a dev and find that downside too much to bother with, thats understandable. However instead of clicking out of this wiki all together there is some info in chapter 2 that I'd highly recommend you looking at. It concerns something called "mixed input", using gamepad and mouse inputs at the same time to play games, and it impacts more than just steam controller users.

One final note for this section; many players in the steam controller and steam input community actually do not like how Valve has tied Siapi to steam. For all the benefits the api represents, and in the context of the modern age where "competition" is a buzz word such that siapi makes steam more valuable as a platform, its hindered by design by not being universal like xinput. Its sad that for their vr stuff, Valve went open source. It would have been amazing for siapi to have been given the same treatment.
