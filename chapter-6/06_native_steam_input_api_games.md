# 06: Native Steam Input API Games

As mentioned in the Intro to SIAPI chapter, some developers have implemented SIAPI into their games. This provides "native" Steam Input support, and therefore "native" Steam Controller support.

Implementing SIAPI into games does have loads of benefits such as
* binding actions instead of buttons
* automatic Action Set swapping based on game context
* in game button prompt glyphs will always match not just your controller but also any customization to the config the player has done
* and many more!

But is it all that amazing? Well... yes and no. As a relatively new input API, some devs have done really good jobs implementing it while others have struggled. It's kind of a spectrum on how good it is, and it would be helpful to the players to know the quality of the SIAPI implementation prior to buying a game.

In this chapter, we'll be developing a rating system to do just that and then rating games in accordance with that system. This will hopefully serve two functions;
* providing the information to the player so they can make an informed purchase
* providing examples for developers who are considering implementing SIAPI into their game, to help them avoid pitfalls and give them a goal to work towards.

We'll also be providing resources for developers to help them implement SIAPI into the games. This will include;
* how to decide if SIAPI is right for your game; while all games can benefit, for some it may be a lot of effort for little gain
* a link to Valve's documentation
* a "best practices" guide from the perspective of a player; what makes it good for us?

With this introduction out of the way, lets talk rating systems.
